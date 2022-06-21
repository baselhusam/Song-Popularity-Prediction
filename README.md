# Song Popularity Prediction Project

## Executiv Summary
This project puts the prediction of the song's popularity in the spotlight. After we've done our analysis and the EDA process and made it prepared, we found that Random Forest Regressor model was the most suitable algorithm for our data, but there were some issues with the data set we had to deal with. <br>
In the beginning, we got rid of the outliers that would mislead our model to incorrect conclusions. And because the skewnesses for some specific columns led to unfair results for the minority data in our model, fixing the shape of the distribution of the numerical features was a very important step. Finally, we split the data set into training and testing and then fitted it to our model to see our results. Finally, we've looked into the R2 score and the RMSE to evaluate our model. <br>

### 1.Introduction
If there is an artist who wants to make a hit song, then it must be popular, but how can we know if a song is going to be popular or not? and what are the main properties that make the song a hit and popular song? Our goal is to determine the factors that help and affect the popularity of the song. With the cloud-based platform’s resources such as RAM, Hard Disk, and the environment, using machine learning algorithms and techniques, we will make a model that can predict the popularity of a song. <sub> <i>(Kanjilal, 2021)</sub></i> <br>

### 2. Methodology
#### 2.1 Model Description
Random Forest is a machine learning algorithm based on ensemble learning, by the decision tree algorithm. It is made for large-scale and complex data analysis. <sub> <i>(Qi, 2012) </sub> </i> we've implied the model with 500 estimators because we've different kinds of scales and a large number of features, so we need a huge number of decisions to make the prediction. after we split the data into features, and target then split them into train and test, we fitted the model with the appropriate train data, then test it by making the predictions with the test data. It was chosen after we've looked into the data visually and statistically and knew that we are dealing with uncorrelated features, because the random forest works only on a subset of features <sub> <i>(Yiu,2019)</sub></i>, and to be honest, random forest is always a great option for modeling. <br>
#### 2.2 Dataset Description
The song dataset is a free source dataset from Kaggle, the main purpose/target of it is the song's popularity. It has 15 features and 18835 records/instances, each feature represents a specific specialty of a song. A brief description of each feature <br>
<ul>
  <li> <b>song popularity:</b> the target column. </li>
  <li> <b>song duration ms:</b> the song duration in milliseconds. </li>
  <li> <b>acousticness:</b> confidence measure from 0 to 1. </li>
  <li> <b>danceability:</b> describe how suitable a track is for dancing. </li>
  <li> <b>energy:</b> movement of energy through a substance in waves. </li>
  <li> <b>instrumentalness:</b> represent the amount of vocals in the song. </li>
  <li> <b>key:</b> a system of functionally related chords. </li>
  <li> <b>liveness:</b> reverberation time. </li>
  <li> <b>audio mode:</b> whether the waves are major or minor </li>
  <li> <b>speechiness:</b> detects the presence of spoken words in a track. </li>
  
</ul>

The dataset is from the musical industry. We've chosen this dataset to make something unserious and show that even in a big project you can make something unusual, the seriously is important but not always. as a part of the youth community, and because the music is the main part of our daily routines, we found it interesting to make this project. <br>
Firstly, we've cleaned the data by finding outliers and handling them, by making a Box-Plot for each feature, and removing the detected outliers. <br>
