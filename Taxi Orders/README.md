# Taxi Orders Prediction

We have a taxi orders data for few monthes of 2018. In porpouse to avoid drivers shortage we need to learn model to predict amount of orders in the next hour. Root mean squared error of prediction should be less then 48. We use linear regression and gradient boosting alghorytms. Time series has a trend and daily seasonality. Lets see how our models are going to handle this task!

## Data Description

## Models
- Linear Regression
- LightGBMRegressor
- XGBRegressor
- FBProphet

## Usage
First of all you should install lightgbm, pystan and fbrophet

```
!pip install lightgbm
!pip install pystan
!pip install prophet
```

##Requirements
python 3
