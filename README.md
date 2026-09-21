This code uses the NOAA and ERCOT public databases to create a multi-factor price model on energy.

First, DAM settlement point prices are collected using the ERCOT API.
Then, the prices are filtered to target Houston, TX as the point of reference.
Then, dummy variables and categorical variables are created for the week, hour, month, and weekend.
Then, data for autoregression is collected on 24, 48, and 168 hour interval.
Then, rolling averages for the 24 and 168 hour interval are collected.
Then, historical NOAA weather data is collected.
Then, the variables are used in a piece-wise decision tree framework with xgboost
Finally, xgboost nonlinear model is compared to naiive ARIMA model to determine value-add.
