# Cab-Booking-Prediction
Python Machine Learning project using scikitlearn,pandas,numpy,matplotlib

# Problem Statement
Build a Machine Learning model to predict the total count of cabs booked in each hour by the new data

Cab booking system is the process where renting a cab is automated through an app throughout a city.Using this app people can book a cab from one location to another location.  
Being a cab booking app company, exploiting an understanding of cab supply and demand could increase the efficiency of their service and enhance user experience by minimizing waiting time.

#### Objective
To combine historical usage pattern along with the open data sources like weather data to forecast cab booking demand in a city.

#### Process Flow: 
You will be provided with hourly renting data span of two years. 
Data is randomly divided into train and test set. You must predict the total count of cabs booked in each hour covered by the testset

# Analysis Approach

## Exploratory Data Analysis
Contains the initial exploration of data like 
*   Load training and testing data into DataFrame
*   Inference about the data -info
*   Find Missing Values
*   Feature Engineering - Create new columns hour,weekday,month
*   Outliers Analysis and removing outliers
*   Correlation Analysis
*   Data Visualization 
    * Univariate
      * Distribution of target variable
      * Distribution of continuous variables
    * BiVariate-Distribution of target variable vs categorical variables
    * Multivariate - Distribution of all continuous variables vs other continuous variables
*   Keep only 1 column for columns having high correlation
*   One-hot encoding/dummification of the categorical variables
*   Dealing cyclic features - hour,month,season,weekday
*   Generating Cramer’s V pairwise matrix plot using `association_metrics` library

## Modeling
* Split the data into training and testing using train_test_split
* Standardize the data by applying fit on training data and transform on train and test data
* Regression algorithms Like 
  * Linear Regression
  * Support Vector Machines(Linear)
  * KNN
  * NaiveBaye's
  * Decision Trees
  * Random Forest
  * Bagging
  * XGBoost,AdaBoost,GradientBoost are used to build the model
  * MLPRegressor
* There is same accuracy for tree based models with and without OneHotEncoding categorical features while accuracy improved for rest on OneHotEncoding
* Feature Importance from the model is also displayed
* Ensembling models like RandomForest and Boosting gave the best results among all the algorithms used

