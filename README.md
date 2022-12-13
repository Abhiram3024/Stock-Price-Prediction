# Stock-Price-Prediction
Stock prices are volatile in nature and price depends on various factors. The main aim of this project is to predict stock prices using Long short-term memory (LSTM) model.

In this project our task is to predict stock prices to help investors predict stock prices to aid their investments. We use the open, high, low and close prices from the datasets to predict the price of a stock.

The LSTM is a sequential model which contains 4 layers which use ReLU activation function. The rectified linear activation function or ReLU for short is a piecewise linear function that will output the input directly if it is positive, otherwise, it will output zero. It is given by f(x)=max (0, x). After each layer we included a dropout layer which helps preventing overfitting. The model is then compiled using Adam optimizer, mean squared error as loss function. Then the model is fit using epoch size as 50 and default batch size of 32. 

We have built our website using Streamlit Python framework which uses the model as a backend. Streamlit is an open-source app framework for Machine Learning and Data Science teams. The user is able to select a Stock Ticker from a drop down which contains the most commonly traded stocks. The time period for the prediction can also be set by selecting the start and end date. The statistics of the stock in this time period is displayed which contains factors such as count, mean, minimum price, maximum price. We calculate moving average of the first 100 and 200 days. If the moving average of 100 days is more than the moving average of 200 days it indicates an uptrend and if it goes below it’s a downtrend. The graph for the same can be viewed on the website.

The prediction of the stocks can be viewed on the website. The price from a certain period of time can also be predicted using the model. The R2 score, mean square error and mean absolute error is also displayed for the same. The R2 score generally lies between 0.80 and 0.95. If the stock prices are volatile and changing abruptly it leads to a decrease in accuracy which may cause the R2 score to go beyond this range.

![input](https://user-images.githubusercontent.com/76044102/207357241-bab2b2b1-f319-4500-9c84-383ba335732e.png)

![Data](https://user-images.githubusercontent.com/76044102/207357327-c89f2823-3b76-4a67-acc0-8c2c50f99296.png)

![Prediction](https://user-images.githubusercontent.com/76044102/207357355-1630d2c7-bad2-4792-95cc-5d14edff2cac.png)
