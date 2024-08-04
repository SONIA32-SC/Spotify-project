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
Data extracted from data sources was cleaned and transformed using numpy and pandas tools together with Python and merged into one dataframe. 

## Exploratory Data Analysis
Merged dataframe was analyzed to detect trends and correlations with features and also between dependent feature(popularity) and other independent features using data visualization tools such as matplotlib and seaborn will be used to visualize results of the analysis. 
Finding included:
1. Instrumentalness does not mean loud song
   ![image](https://github.com/user-attachments/assets/b260951e-5d9f-425e-a385-482e08205d42)

2. Long songs are not popular songs
   ![image](https://github.com/user-attachments/assets/06795d27-fbbf-4ada-b278-0d136b7a4f03)

3. Popular songs have low acousticness
   ![image](https://github.com/user-attachments/assets/7c3341a1-bfb5-4c14-947c-b7ca1ca7fb81)

4. Most popular song genre is pop
  #### The genres of the first 20 most popular songs
  ![image](https://github.com/user-attachments/assets/84367611-d8cd-40df-a258-abe56ecf1f55)
  
### Heatmap
![image](https://github.com/user-attachments/assets/d8c88ea6-989a-4df8-b5a1-f93651ddb430)

 From the Heatmap above, popularity is:
a. not correlated to tempo
b. weakly correlated to danceability and loudness.
c. negatively corelated to acousticness, liveness,instrumentalness, duration_min, GDP_year, GDP
d. strongly correlated to year

## Modelling
Three models were built after categorical feature were transformed into numerical features with OneHotEncoder and numerical columns were scaled with StandardScaler. The performance of each model was assess

1. Ridge Regression
   
![image](https://github.com/user-attachments/assets/6574b079-483b-46da-b3ad-fece7d2fed76)

2. ElasticNet
   
![image](https://github.com/user-attachments/assets/31832a1a-5340-4d6d-aa8f-341e03272b32)

3. DecisionTree Regressor
   
![image](https://github.com/user-attachments/assets/564c8c9d-89dd-49bd-8122-9796c4ff84c0)

## Model Evaluation
After using cross validation to fit each model. Below is the perfromance observed

The best model is the Ridge Regression model

### Observations during model creation
While developing the models, it was observed that dropping categorical feature (genre) from the feature list used to build the model makes the model perform poorer whwereas building models with all the features in the dataset improves model performance

## Recommendations
1. The popularity of songs is influenced by the year song was posted on Spotify. Spotify songs have gained more popularity in recent years than they did in previous years.
![image](https://github.com/user-attachments/assets/8242d75d-2a9e-4460-81d4-2fb533c01e64)

2. Tempo does not influence song popularity
![image](https://github.com/user-attachments/assets/6f3f453b-bbc0-4cf9-9b7b-e8c273da6231)

## Further work
Further work on this project must focus on improving the current model by increasing the data.












 





   













