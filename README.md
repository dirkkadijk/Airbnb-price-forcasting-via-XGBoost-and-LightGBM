# What factors influence the price of Airbnb rental most, based on XGBoost and LightGBM machine learning?

by Dirk Kadijk, Data Scientist of DGK IMPAKT Consulting


## Table of Contents

1. Installation
2. Project Motivation
3. File Descriptions
4. Results
5. Licensing, Authors, Acknowledgements



## 1. Installation

Install beyond the Anaconda distribution of Python (a range of sklearn modules are used): lightgbm 2.3.0 and xgboost 0.90.

The code is in Jupyter Lab notebooks, and they include modules which loads supporting _.py files. The code should run with no issues using Python versions 3.7.



## 2. Project motivations

In this project Airbnb day prices in Seattle for 2016–2017 are predicted using data analysis and feature engineering. 
We apply and compare the machine learning methods Random Forest regressor and the 2 boosting methods Light Gradient Boosting (LightGBM) and XGBoost to see which features in the dataset influence the price the most.
These models can help hosts establish appropriate rental prices and also to find out what features can influence rental price the most to improve revenue.

The underlying reason and focus for this project is to practice the CRISP-DM process step 'Evaluation - Communicate the business insights' via:
 - Create a Github repository to share your code and data wrangling/modeling techniques, with a technical audience in mind
 - Create a Medium blog post to share your questions and insights with a non-technical audience


## 3. Data source

We use data from from kaggle Seattle Airbnb open data to take a closer look at this question:
- the `listings.csv` file gives insights about a host, location, review rating score, room and property type;
- and the `calendar.csv` file is about availability and price per each day in 2016–2017 years.

The Seattle AirBnB homes data can be downloaded via the [this link](https://www.kaggle.com/airbnb/seattle/data). 


## 4. Summary of the results

The project is worked out in the Jupyter Lab notebook `Airbnd_price_modelling_by_DirkKadijk.ipynb` with the structure:
1. Introduction
2. Data Assessment and Preparation
3. What month and neighbourhood has the highest daily prices?
4. What other features are important for daily prices prediction? Feature selection
5. What machine learning model performs better (Random Forest, LGBM, XGBoost)?
6. Conclusions

The outcomes are:
- The Airbnb prices in Seatle depend highly on time of the year and neighbourhood. The highest prices are charged in the summer (Jun-Aug) and the most expensive neighbourhood is Downtown.
- The Light Gradient Boosting (LGBM) model and XGBoost model score a similar accuracy score: R-squared crossvalidation scores of **68%** and r2-score of **72%**. And score a few percent higher than the Random Forest model.
- The advantage of the LGBM model is that it has a broad set of features which are important in the model with as the most dominant: **latitude, month, totalrooms, longitude, reviews_per_month, street, amenities_length.**
- This suggests that the LGBM model is the more robust model, however one can use both models and compare (or average) the price forecasts.

The Medium blog with a summary of results with the visuals you can find [here](xxxxxx)


## 5. Licensing, Authors, Acknowledgements

Must give credit to Airbnb Inside which is an independent, non-commercial set of tools and data that allows you to explore how Airbnb is really being used in cities around the world.