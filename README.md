# bicycle_users_prediction
Predicting the number of bicycle users in particular hour of the day, given the weather conditions, date, and time.

We have hourly data for 2011-2012. Dataset is relatively small, clean and already
clipped/normalized.
● Exploratory Data Analysis (EDA) and feature engineering/selection are conducted
● Dropped some unnecessary variables and values and encoded the categorical variables.
● Four models are built in which XGBoost and Deep Learning show the best results.
● We can improve the results by acquiring more data, creating more feature, and ensembling/stacking.

This is a quick glance in the data:
[weathersit, weekday, season] are categorical variables with fairly even distribution.
[holiday, workingday] are boolean variables. 
[atemp, temp, hum, windspeed] are weather condition variables with fairly normal distribution.
Number of bicycles users is heavily right skewed. It would  benefit from transformation.
The very right tail could include some outliers. 
More than 93% of the records are less than 500
Correlation for the numerics variables are investigated. 
Target has a strong correlation with [temp, hr, month, hum]
[hum] has 13 missing rows which we dropped.
temp & atemp are strongly correlated. We dropped the temp.
