# Predicting Wildfire Activity in the United States 
Author: Abirami Valliammai Kathiresan

Course: STA 141A

## Overview
The goal of this project is to develop predictive models that will forecast the likelihood of notable wildfires occurringin the US. 
Historical wildfire data is transformed to create records of 1° × 1° geographic cells for a given month.

## Dataset 
Spatial Variables: latitude, longitude, state
Temporal Variables: month, year
Lagged Fire History Variables: fire count this month, fire count lag 12, rolling fire counts over past 3 months, rolling fire counts over the past 12 months, rolling average fire size over past 3 months, and rolling average fire size over past 12 months.
Fire Attirbute Variables: fire cause (natural, human, infrastructure), average fire duation, land ownership type (federal, public, private)

## Model Fitting
The two models used are:
1) Logistic Regression (baseline):
   Helpful for binary classification and assumes a linear relationship among predictors
3) XGBoost (gradient boosting):
   Uses decision trees to inform predictions and caputres underlying nonlinear relationships among predictors

## Evaluation
The models were evaluated using time-awareness validation since they were trained until a certain year and the following year was used as the validation. 
AUC and ROC plots were compared to determine which model performed better 

## Results
1) Logistic Regression AUC: 0.722
2) XGBoost AUC: 0.831

The XGBoost model outperformed the logistic regression model by 10.85%, suggesting that it better understands the complex interactions among the predictors and the nonlinear nature of the geographic and temporal trends. 
