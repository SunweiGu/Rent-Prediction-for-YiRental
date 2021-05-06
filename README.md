# Rent Prediction for Yirental

The repository contains files ‘  ‘, which provides the dataset …, and file ‘  ’, which provides the code for data cleaning, modeling and visualization.

## Project Overview

The project aims to help Yirental, an online housing rental platform to provide a better rental pricing experience for renters and homeowners. To achieve this goal, our team proposed an interactive UI panel that allows the users at Yirental to choose the customized value for each feature (house type, room number, location, etc.) and then it will generate the prediction for the user. The UI panel is designed as the front-end of this minimum viable product while the back-end is supported by the supervised machine learning model, which was selected by our team based on the prediction accuracy.


## Background

About Yirental (https://www.yirental.com) : 
Yirental was founded in 2017 out of Seattle, and has been dedicated to optimizing the rental experience for tenants, homeowners, property managers and so on. So far, Yirental has helped over 40,000 users find rental accommodations across several countries.

Data Description: 
For this project, Yirental Inc. provides us with its historical raw data from year 2017 to 2021 that covers more than 9,000 listings’ records across the U.S.. In the dataset, each record contains information including the property’s types, number of rooms, its geographic location, posting date, which total in 51 columns. 



## Problem & Motivation

The motivation of this project came from our own experiences. When we were looking for apartments in a new city, we always wanted to find the best price deal while making sure it is a convenient location. However, the price range typically varies largely for similar properties, and makes it hard to choose the right one. 

The problem we aim to conquer is rational rent pricing for apartments and houses. When it comes to price a certain property, the rent price largely depends on the location, the time of the year, the property type, and many other factors. From the renters perspective, they are struggling to find the best location while spending the least amount of money as they are unfamiliar with the local housing market and very likely to overpay to waste money. For the house owners, they are having a hard time pricing the property as they want to find the balance between maximizing income and still making sure the property is attractive to renters so it won’t be empty to waste money. Through this project, we want to solve both of the renters’ and house owners’ problems with rent pricing.


## Solution

After data processing and cleaning, we totally have fifty variables, including ten continuous variables, thirty-four categorical variables and six datetime which means our features are mainly categorical variables. 
About our modeling, we have implemented eight different models, including Ordinary Least Squares, Lasso regression, CART with Cross Validation, Random Forests, XG Boosting, Gradient Boosting, AdaBoost and Neural Network. We randomly selected 70% of the total data to build our training set. The Ordinary Least Squared model trained returns an R-square value of 0.480, meaning that Ordinary Least Squared model has about 48% of the chance to approximate the actual data points. This R-square value is lower than we expected. We found that the model of Gradient Boosting performance is the best. In this model, there exist three important features, including the amount of bedroom, the amount of bathroom and the city of New York. The Gradient Boosting models’ mean absolute error is almost four hundred and forty-four, and its mean squared error is over four hundred thousand. However, the model of Ada Boosting performance is the worst, the Ada Boosting models’ mean absolute error is six hundred and fifty-six, its mean squared error is almost one million and three hundred thousand. 
Finally, we choose Gradient Boosting to create our model.

## Result

## Requirement

 - python >= 3.7.3
 - Geographiclib   ==    1.50
 - Geopandas   ==   0.9.0
 - geoplot   ==   0.4.1
 - geopy   ==    2.1.0
 - Keras   ==   2.4.3
 - Keras-Preprocessing   ==   1.1.2
 - matplotlib   ==   3.2.2
 - numpy   ==   1.20.1
 - pandas   ==   1.0.5
 - scikit-image   ==   0.16.2
 - scikit-learn   ==   0.23.1
 - scipy   ==   1.5.0
 - seaborn   ==   0.10.1
 - tensorflow   ==   2.4.1
 - tensorflow-estimator   ==   2.4.0
 - xgboost   ==   1.4.0


