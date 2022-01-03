# Combining Predictive Techniques with Alteryx

## Dataset

This dataset contains store sales data, store information and store demographic data.

## Summary of Tasks

1. Determining Store Formats for Existing Stores
2. Predicting Formats for New Stores
3. Predicting Produce Sales

## Key Insights

First, I determined store segments for existing stores by clustering with the K-Means Clustering method which calculated the Adjusted Rand and Calinski-Harabasz indices based on the sales data and more specifically category sales as a percentage of total store sales. The optimal number of store formats according to the highest median was 3.

Here are the locations of the stores, colored by the cluster and sized by total sales.

![Store segments](https://github.com/currentco/data-analytics/blob/main/store_formats/tableau_viz.png)

In the second task for new store format prediction I used demographic and socioeconomic characteristics of the population that resides in the area around each new store and also the existing stores to make the predictions. I then compared the fit and error results of a decision tree, a random forest and a boosted model and decided to choose random forest model based on these results. The training sample was 80% and validation sample 20%. I could have used PCA to reduce the number of predictor variables but there was no need and all the variable were included as is.

In the third stage for forecasting the sales data for new and existing stores I used Time Series modeling. First, I decomposed the sales data and analyzed the seasonality, trend and error plots. For the ARIMA model I also had to make the data stationary with seasonal differencing. Then I compared the ETS and ARIMA models against the 6-month holdout sample and the ETS delivered more accurate results with lower RMSE. I decided to go with the ETS model after this comparison.

Here's a graph of the excisting and forecasted sales.

![Sales forecast](https://github.com/currentco/data-analytics/blob/main/store_formats/tableau_viz_sales.png)

## License

Copyright (c) 2021 Eevamaija Virtanen

This project is licensed under the terms of the MIT license.
