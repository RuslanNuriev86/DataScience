# Interactive Air Quality Monitoring Map
![Screen](https://user-images.githubusercontent.com/92801594/148647174-1b15c405-3e8c-48c4-803b-ddd755d2c080.jpg) <br />
[Check out the Interactive Map here](https://moscow-air-monitoring.netlify.app)

### Data Engineering <br />
At the beginning we have many files contaning information from Moscow's air quality monitoring stations such as concentration of CO, N, NO2, PM10, PM25, temperature, pressure, humidity, precipitation, temperature at different heights from Ostankino tower("profilemer") of 2020. So a goal of this part is to prepare data for analisys and machine learning. After proceedings during this part the whole data saved as convinient dataframe csv files and ready for a further analisys.

### Model Tuning 
At this part we picked from catboost import CatBoostRegressor, Pool
 as a model algorithm. Fitted a model on one of the datasets and fin out the best parameters like max depth, learning rate, max lag and moving average size. <br />
![Autocor CO](https://user-images.githubusercontent.com/92801594/148649539-4d8342e5-68f2-40b2-9554-e5a13623829d.jpg)
![Autocor NO2](https://user-images.githubusercontent.com/92801594/148649556-e1b572ea-33c4-470c-9c1e-f08266b9ffe9.jpg)
```
{'estimator__depth': 3, 'estimator__iterations': 50, 'estimator__learning_rate': 0.3}
```

### Machine Learning
We've built models to predict indicators of air quality such as CO, NO2, NO, PM10, PM25 for 9 monitoring station of Moscow for the next day (12 hours of 31st December, in this case). Mean absolute percentage error most of them is less than 10%.

```
test_MAPE NO2      0.032898
CO       0.163103
PM2.5    0.039741
NO       0.102650

test_SMAPE NO2      0.036472
CO       0.669831
PM2.5    0.045575
NO       0.156696
```
![Prediction NO](https://user-images.githubusercontent.com/92801594/148650084-5419534f-1b3f-4c28-8f1f-c20a35330284.jpg)
![Prediction CO](https://user-images.githubusercontent.com/92801594/148650096-8445a490-b472-4a83-8170-44486dffdddb.jpg)
![Prediction PM25](https://user-images.githubusercontent.com/92801594/148650104-9227f3e0-5127-4a0b-b897-0ebc6424d1e5.jpg)

### Map Creating
Since we get forcasts of indicators of air quality for a next day for few monitoring stations of Moscow it's time to put them on the map!
We can get forecast of air quality for the next day by clicking markers up. Also we can see names of monitoring stations by tipping markers.
[Check out the Interactive Map here](https://moscow-air-monitoring.netlify.app)
