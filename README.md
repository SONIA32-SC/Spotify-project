# How popular can your music get on Spotify?
![image](https://github.com/user-attachments/assets/b881a7a7-f528-4099-9f79-90ac869ff305)


Spotify is the fastest growing digital music service platform that gives access to millions of songs. Spotify maintains several playlists that feature the most streamed songs across different time frames. Spotify requests that music lovers purchase a range of subscription packages which will allow them to play songs of their choice at their convenience. Music artists are then paid an amount depending on where their music is played, their listeners subscription type and how often their songs are streamed. Spotify pays by streamshare and not by song, therefore for an artist to benefit financially from spotify, their song must be streamed many times. Music distributors and record labels may also have a share in these financial rewards depending on the contract between music artists and Spotify. It will therefore be beneficial for artists, record label managers and music distributors to concentrate on not only giving their song a global appeal but also make music that listeners will love to listen to repeatedly. 

This project seeks to help artists, music distributors and record label managers maximize financial benefits from their association with Spotify by building a model that will help predict songs that will generate global appeal and cause them to be streamed repeatedly based on the structure of the song alone. This model will be able to predict marketable songs even before they are released and uploaded onto Spotify. 

## Data Sources
Main dataset
Kaggle Spotify 1 million tracks 
(1159796 rows and 11 columns)

Supplementary dataset
Annual GDP of the United States from 1929 to 2023 
(5 rows and 96 columns)

## Data Cleaning
Data extracted from data sources was cleaned and transformed using numpy and pandas tools together with Python and merged into one dataframe. After data wrangling the resultaing features were genre, danceability, loudness,acousticness, instrumentalness,tempo,year, popularity, duration,GDP year and GDP. Popularity was the dependent feature and it had a left skewed with along tail distribution.

![image](https://github.com/user-attachments/assets/177b091b-bb63-4e74-960b-ebf8fc1d0883)


## Exploratory Data Analysis
Merged dataframe was analyzed to detect trends and correlations with features and also between dependent feature(popularity) and other independent features using data visualization tools such as matplotlib and seaborn. Line plots and and a heatmap was generated to visualize results of the analysis. 

Finding included:

1. EDA showed that the song feature, instrumentalness, was not related to loudness and this is evident from the lineplot.
 
   ![image](https://github.com/user-attachments/assets/7c68c110-6d66-42ce-8cf3-f426848a3980)


2. Songs with longer durations are not popular songs and this is shown in the graph below

   ![image](https://github.com/user-attachments/assets/0534b6bc-285f-46f2-95d9-9e0021f91129)


3. EDA also showed that popular songs have low acousticness

   ![image](https://github.com/user-attachments/assets/faf363d6-e467-426f-b934-c8590a15b9d4)


4. Most popular song genre is pop
   
  #### The most popular song genre was pop and this was evident from the first 20 most popular song list shown below

  ![image](https://github.com/user-attachments/assets/a404f4a7-d024-4051-932c-0999034d0dba)


  
### Heatmap

![image](https://github.com/user-attachments/assets/a5f320f6-78a5-4d98-ae8a-13977fbad6e9)


 From the Heatmap above, popularity is:
a. not correlated to tempo
b. weakly correlated to danceability and loudness.
c. negatively corelated to acousticness, liveness,instrumentalness, duration_min, GDP_year, GDP
d. strongly correlated to year

### Muticollinearity detection from the heatmap
The heat map also revealed strong relationships between some of the independent features.

1. Acousticness vrs loudness

   ![image](https://github.com/user-attachments/assets/607ce93f-66dd-4f0a-8255-b65f4c881952)


2. Instrumentalness and loudness
   
   ![image](https://github.com/user-attachments/assets/0c12864b-7f2e-44c6-9ac5-daf8a5b284d5)


4. GDP year vrs GDP
   
   ![image](https://github.com/user-attachments/assets/f5aa0a25-27fb-44ec-86a7-f297e8527286)


## Modelling
Four models were built after categorical feature were transformed into numerical features with OneHotEncoder and numerical columns were scaled with StandardScaler. Three were linear models and one was a non_linear model.

1. Ridge Regression  2. ElasticNet 3. DecisionTree Regressor 4. Random Forest( non_linear)
  

## Model Evaluation

After using cross validation to fit  and assess the three linear models built,  Ridge Regression model showed the highest r2 value when compared to the other models. This indicates that the model works better than all the other models evaluated at this stage of the project. It also showed the lowest MAE and MSE scores and this indicates reveals that it performs with minimal errors compared to the other models evaluated.


![image](https://github.com/user-attachments/assets/2dbbcdf1-d840-4cf5-abb3-3dd04cca838f)  ![image](https://github.com/user-attachments/assets/f958ef67-15f8-403f-a351-efb522c1e82c)


The Random Forest moddel  with 8 n_estimators performed poorly. It  showed very low accuracy and F1 scores.The area under the curve was 0.21 which signifies that model is performing poorly.

![image](https://github.com/user-attachments/assets/4386b846-9c8d-43c3-8da7-50c0bd009fbd)


These graphs show that the best model is the Ridge Regression model because it has the highest R-squared score and the lowest Mean absolute error(MAE) and Mean squared error(MSE).

### Ridge model improvement
The current performance of the Ridge Model shows that although the Ridge model is the best model built so far for this project, there is more  room for improvement. Increasing number of features in the data could improve model performance significantly.

![image](https://github.com/user-attachments/assets/7740e753-fba7-4dac-aeeb-bc35822a34af)



## Important features of Ridge Model.

All the features in that data were equally important to the Ridge model. This further indicates that increasing data volume and features could lead to better model performance.
Acquiring more data will improve the robustness of model ,e nhance generalizations and lead to better feature engineering while offering deeper insights

![image](https://github.com/user-attachments/assets/be15ace8-7c2a-4da5-9324-5f9bfaeceb79)
















 





   













