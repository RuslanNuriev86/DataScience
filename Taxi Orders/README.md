# Taxi Orders Prediction

![new-york-city-tlc-taxi-stock1_2040 0](https://user-images.githubusercontent.com/92801594/156035920-48aea278-3311-44b0-beae-63ffdb70fd00.jpg)
Source: theverge.com

We have a taxi orders data for few months of 2018. In porpouse to avoid drivers shortage we need to learn model to predict amount of orders in the next hour. Root mean squared error of prediction should be less then 48. To do that we going to use linear regression and gradient boosting alghorytms. We also keepin mind that the data has a trend and daily seasonality. Let's see how our models are going to handle this task!

## Data Description

num_orders - number of orders

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

## Requirements
python 3
