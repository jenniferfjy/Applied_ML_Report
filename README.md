# Bike-Sharing-Demand-Forecast

![Bike Sharing](https://images.ctfassets.net/p6ae3zqfb1e3/33ZjKWPEMX1FLn2X8XZurc/4b1c383d920c7227e052ff001511647f/CaBi_Ride_experience_Hero_2x.png?w=2500&q=60&fm=webp)

This repository contains code and data for a bike sharing demand forecasting project. Bike sharing systems are becoming increasingly popular in urban areas, and accurate demand forecasting is essential for managing resources efficiently. This project aims to predict bike rental demand based on historical usage patterns and various features.

## Table of Contents

- [Introduction](#introduction)
- [Data](#data)
- [Exploratory Data Analysis](kaggle_bike_sharing_demand_data_exploration.ipynb)
- [Final Report](Applied_ML_Report.pdf)
- [Codes](all_models.ipynb)

## Introduction

Bike-sharing systems are gaining popularity in major cities. The process of renting a bike through an app on the users’ smartphone yields lots of information for the provider. Particularly important is the number of bikes rented within a given time period, so that the provider can make proper adjustments to meet the demand. In this project, we analyzed hourly data from Capital Bikeshare in Washington, D.C. over a span of two years and took two distinct approaches to predict future demand. The best regression model HGBT achieved an R2 of 0.8928 on the validation and an RMSLE of 0.4652 on the hidden testing set. The best time series (LSTM-based) model achieved an R2 of 0.9505 and an RMSLE of 0.4540 on the validation and test respectively, which ranks top 27% among all submissions on Kaggle.

## Data

The dataset provided by Fanaee-T and Gama (2023) includes Capital Bikeshare’s hourly bike rental data spanning two years with the corresponding weather and seasonal information. The dataset contains two files, train.csv, and test.csv, with 10,887 and 6,493 rows respectively. Both files comprise four categorical variables and eight quantitative variables.

## Exploratory Data Analysis

After parsing datetime, we drew a heatmap to drop highly correlated features. Then, we plotted the distribution of our target total and decided to treat log(total) as our new target as it’s skewed.

We also plotted several boxplots as shown above against the target by different features and found that the key observation are:
- The peak of the rental time is 8 am and 5 pm to 6 pm during weekdays.
- More rentals are in fall but fewer in spring.
- Rentals generally decrease as wind speed and humidity increase.


