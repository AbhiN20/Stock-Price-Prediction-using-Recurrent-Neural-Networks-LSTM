# Stock-Price-Prediction-using-Recurrent-Neural-Networks-LSTM

Stock Price Prediction of Apple Inc. Using LSTM Recurrent Neural Network

# Dataset:
The dataset is taken from yahoo finance (yfinance python package). The dataset always consists of Date, Open, High, Closing Price (Close), Adjusted Closing Price (Adj Close) and Volume of Apple Inc. stocks from 1st january 2005 to 10th September 2023 - total 4703 rows.

# Price Indicator:
I'm using closing price time series moving average for predicting the stock prices.

# Data Pre-processing:
Considering Daily Return (using percentage change) and Cumulative Return (using 1+Daily Return). Scaling the dataset so all values have been normalized between 0 and 1 using MinMax Scaler. Splitting the dataset into training and validation sets (for testing purpose).

![image](https://github.com/AbhiN20/Stock-Price-Prediction-using-Recurrent-Neural-Networks-LSTM/assets/122420588/9d5c8f2c-1eff-4ea7-95e9-1fbf501fcb2d)

# Model:
The model architecture consists of two LSTM layers, each with 50 memory cells, followed by dropout layers to prevent overfitting. Dropout randomly "drops out" a portion of neurons during training, making the model more robust.

Two dense layers are added for processing and making predictions. The final dense layer has one neuron, which predicts the next stock price.


# Training:
80% data is used for training. Adam (adaptive optimization algorithm) optimizer is used for adjusting learning rates during training to improve convergence. It is well-suited for training deep neural networks like the LSTM.

![image](https://github.com/AbhiN20/Stock-Price-Prediction-using-Recurrent-Neural-Networks-LSTM/assets/122420588/b14b1cdf-2aea-4ef0-98ee-9583e7372519)


# Train/Test Accuracy:
Train/Test accuracy metric is root mean square error (RMSE) which measures the difference between predicted and actual stock prices. The goal is to minimize this loss during training.
![image](https://github.com/AbhiN20/Stock-Price-Prediction-using-Recurrent-Neural-Networks-LSTM/assets/122420588/af6da682-aefc-44d2-8e4b-20236656ee8f)

# Results:
The comparison between original stock price and predicted price during validation period:

![image](https://github.com/AbhiN20/Stock-Price-Prediction-using-Recurrent-Neural-Networks-LSTM/assets/122420588/962690c0-c8eb-4c6d-b0ee-f375f730beb4)


After the training the fitted curve with original stock price:

![image](https://github.com/AbhiN20/Stock-Price-Prediction-using-Recurrent-Neural-Networks-LSTM/assets/122420588/82a561d1-3e39-4023-bcad-e85bb964c856)


# Observation and Conclusion:
I used only closing price as an indicator to build the model and prediction. The testing RMSE was: 0.043 which is pretty good to predict future values of stock. Stock price of last day of dataset was 178.1799 and predicted stock price was 177.9638. However, future values for any time period can be predicted using this model.

Finally, this work can greatly help the quantitative traders to take decisions.

