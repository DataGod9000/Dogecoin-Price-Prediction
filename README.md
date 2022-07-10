
# Dogecoin Price Prediction

This project uses LSTM to do a time series prediction of the price of Dogecoin in the following day. For example, if I am running this test on 1st Jan 2022, the price prediction will be for 2nd Jan 2022. 




## Data

Historical time series data which includes information like the daily closing and opening prices of Dogecoin is acquired from Yahoo 
via Pandas Remote Data Access. 60 days worth of data prior to the date of prediction is used to make the eventual prediction of Dogecoin price on the target date. 
## Model

Model of Choice: LSTM

The deep learning Recurrent Neural Networks (RNN) is perfect for time series prediction like this one because the model does a good job at
learning long term dependencies in data. As we are working with a big historical data set, which can potentially
be even bigger, LSTM works wonder by retaining and processing important information in the data, while forgetting the less 
important ones. 

The result sees that our predicted price follows the general trend of the actual price, which suggest that our prediction is
accurate. Our RSME score confirms this as it shoes that our model has an average error of USD$0.045 on our training set, and an average error of
USD$0.055 on our test set.

| Train Score (RMSE) | Test Score (RMSE) |
| ------------------ | ----------------- |
| -0.045             | -0.055            |


## Limitations and Futureworks

A prediction of prices a day into the future is not very meaningful when it comes to actually using this prediction for trading. While a longer timeframe prediction can be conducted instead, low accuracy in predict price will be expected as seen in the graph below of predicted price 60 days into the future. The solution for this problem is the inclusion of Sentimental Analysis to increase accuracy of predicted data. For example, an analysis that account for whenever Elon Musk tweets about Dogecoin. 