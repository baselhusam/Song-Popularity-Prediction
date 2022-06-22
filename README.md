# Song Popularity Prediction 

## Executiv Summary
This project puts the prediction of the song's popularity in the spotlight. After we've done our analysis and the EDA process and made it prepared, we found that **Random Forest Regressor** model was the most suitable algorithm for our data, but there were some issues with the data set we had to deal with. <br>
In the beginning, we got rid of the outliers that would mislead our model to incorrect conclusions. And because the skewnesses for some specific columns led to unfair results for the minority data in our model, fixing the shape of the distribution of the numerical features was a very important step. Finally, we split the data set into training and testing and then fitted it to our model to see our results. Finally, we've looked into the R2 score and the RMSE to evaluate our model. <br>

### 1.Introduction
If there is an artist who wants to make a hit song, then it must be popular, but how can we know if a song is going to be popular or not? and what are the main properties that make the song a hit and popular song? Our goal is to determine the factors that help and affect the popularity of the song. With the cloud-based platform’s resources such as RAM, Hard Disk, and the environment, using machine learning algorithms and techniques, we will make a model that can predict the popularity of a song. <sub> <i>(Kanjilal, 2021)</sub></i> <br>

### 2. Methodology
#### 2.1 Model Description
Random Forest is a machine learning algorithm based on ensemble learning, by the decision tree algorithm. It is made for large-scale and complex data analysis. <sub> <i>(Qi, 2012) </sub> </i> we've implied the model with **500 estimators** because we've different kinds of scales and a large number of features, so we need a huge number of decisions to make the prediction. after we split the data into features, and target then split them into train and test, we fitted the model with the appropriate train data, then test it by making the predictions with the test data. It was chosen after we've looked into the data visually and statistically and knew that we are dealing with uncorrelated features, because the random forest works only on a subset of features <sub> <i>(Yiu,2019)</sub></i>, and to be honest, random forest is always a great option for modeling. <br>

#### 2.2 Dataset Description
The song dataset is a free source dataset from **Kaggle**, the main purpose/target of it is the song's popularity. It has 15 features and 18835 records/instances, each feature represents a specific specialty of a song. A brief description of each feature `hello` <br>
 
  * `song popularity`: the target column. 
  * `song duration ms`: the song duration in milliseconds. 
  * `acousticness`: confidence measure from 0 to 1. 
  * `danceability`: describe how suitable a track is for dancing. 
  * `energy`: movement of energy through a substance in waves. 
  * `instrumentalness`: represent the amount of vocals in the song. 
  * `key`: a system of functionally related chords. 
  * `liveness`: reverberation time. 
  * `audio mode`: whether the waves are major or minor. 
  * `speechiness`: detects the presence of spoken words in a track. 
  
  
The dataset is from the musical industry. We've chosen this dataset to make something unserious and show that even in a big project you can make something unusual, the seriously is important but not always. as a part of the youth community, and because the music is the main part of our daily routines, we found it interesting to make this project. <br>
Firstly, we've cleaned the data by finding outliers and handling them, by making a Box-Plot for each feature, and removing the detected outliers. <br> <br>

![Alt text](https://github.com/baselhusam/Song-Popularity-Prediction/blob/main/Images/Screenshot%202022-06-22%20020401.png "BoxPlot Figure For All Columns") <br> <br>
Then, we continued our analysis by looking for skewness in columns by making histograms for each column <br> <br>  
![Alt text](https://github.com/baselhusam/Song-Popularity-Prediction/blob/main/Images/Screenshot%202022-06-22%20020529.png "Histogram Figure For All Columns") <br><br>
then fixing this skewness by applying a kind of transformation called the square root transformation to reduce the difference between features. <br><br>
![Alt text](https://github.com/baselhusam/Song-Popularity-Prediction/blob/main/Images/Screenshot%202022-06-22%20020621.png "The Distribution After The Transformation") <br><br>
After that, we applied the **Min-Max Scaler normalization** for some features that have a different scale than others. Finally, we looked into the correlation between features by making a heatmap plot using the seaborn library. <br> <br>
![Alt text](https://github.com/baselhusam/Song-Popularity-Prediction/blob/main/Images/Screenshot%202022-06-22%20020642.png "Heatmap Figure For Correlation Between Features") <br><br>

### 3. Result and Discussion
For us, as a regression project, the best metrics to evaluate our model are the `R2 score`, and the `RMSE` (Root Mean Squared Error). After we've set our hyperparameters for our Random Forest model for the `n_estimators` as `500`, we concluded the results below:
#### Quality Of The Model
| R2 | RMSE |
| --- | --- |
| 0.4168 | 16.58 |

#### Computational Metrics
| RAM (GB) | Time Spent (m) | Hard Disk (GB) |
| ---- | ----- | ----- |
| 3.38 | 1.7 | 38.72 |


<br> 

As we can see the `R2` score for our model is almost 0.42 which means that we can predict about 42.0% from the data by this model.
The `RMSE` is almost 16.5 which means that the predictions from the model will be far from the actual value maximum of 16.5, either higher than the actual value or lower. <br>
For Computational Metrics we found that we used from the google colab environment about 3.38 GB of **RAM** and 38.72 GB of **Hard Disk**, and it took 1.7 minutes to **build and fit our model with the data we have.** <br>

### 4. Conclusions
Here, we have come to the end of the project. The purpose of this research was to identify the popularity of a song. We tried many machine-learning algorithms and found out that the best algorithm and well-suit model for our data is the Random Forest algorithm. We faced many challenges in some of our features like `Instrumentalness` feature where almost all the records were outliers. But on the other hand, we did our best trying to manipulate the data to reach the highest accuracy possible for our model. <br>
As a result, we achieved a stunning Root Mean Square Error `RMSE` which equals 16.58, and here is the features importance percentage in our data: <br> <br>
![Alt text](https://github.com/baselhusam/Song-Popularity-Prediction/blob/main/Images/Screenshot%202022-06-22%20020816.png "Features Importance For The Model") <br> <br>
We found that the `loudness` has the highest importance for our model, so we can conclude that the more the song is loud the more the probability to be a popular song. <br>
The `key`, `audio_mode` and `time_signature` features have the least importance for the model, maybe that is because the number of unique values in these features is very small. <br>
We do hope that our project will be interesting and maybe even knowledgeable. <br>

### Refrences
1. Kanjilal, J., 2021. Benefits and drawbacks of AI in cloud computing. [online] SearchCloudComputing. Available at:
https://www.techtarget.com/searchcloudcomputing/tip/Benefits-and-drawbacks-of-AI-in-cloud-computing <sub> [Accessed 31 May 2022]. </sub> <br>
2. Qi, Y., 2012. Random forest for bioinformatics. In Ensemble machine learning (pp. 307-323). <sub>Springer, Boston, MA.</sub> <br>
3. Yiu, T., 2019. Understanding Random Forest. [online] Medium. Available at: https://towardsdatascience.com/understanding-random-forest-58381e0602d2 <sub>[Accessed 31 May 2022]. </sub><br>


#### Date
6 / 22 / 2022

&copy; <i> Basel Mather 2022 </i>
