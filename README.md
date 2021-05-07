# Rent Prediction for Yirental

The repository contains files ‘Housing_info.csv‘, which provides the raw dataset, and file ‘IEOR290_ProjectCode.ipynb’, which provides the code for data cleaning, modeling and visualization. 'Housing_info_withgeo.csv' and 'UShousing_info.csv' are supporting files which save intermediate results that can help shorten the running time.

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

After data processing and cleaning, we totally have fifty variables, including ten continuous variables, thirty-four categorical variables and six datetime which means our features are mainly categorical variables. We randomly select 70% of the total data to build our training set. MSE and MAE are performance metrics used for the model evaluation.

About our modeling, we have eight different models, including Ordinary Least Squares, Lasso regression, CART with Cross Validation, Random Forests, XG Boosting, Gradient Boosting, AdaBoost and Neural Network.  We implement all the models and tune parameters to improve the model performance.

Finally, we choose Gradient Boosting with seleted features to create our UI. We may further improve the model performance in the future to find the best prediction model and link it with the map to improve the user experience.

## Use Interface and result

Our User Interface, which is a web-based application, combines the final Gradient Boosting model with a stepwise selection. Since there are too many categorical features that may affect user experience when they are inputting. We decided to select 6 most relevant features for now to design the UI. Pickle is used for storing our model, and Flask is used for interacting the HTML with our model. Internal Yirental users may use it for now to compare the estimated market price to the price landlords listed to make suggestions on price adjustment. This model is flexible enough to include external features that our stakeholders feel important and enables inputting in our UI page in the future. At last, we would pass on the prediction model to Yirental to integrate in their own systems and templates. In the future, this prediction function may be combined with a map (pin for rent prediction) and published to users.

## Requirement

Dataset: the shape of the orginal dataset: (9189, 64). There are 9189 observations and 64 features. One observation indicates one leasing post on the website.

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


