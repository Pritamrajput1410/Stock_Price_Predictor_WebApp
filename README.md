# Stock_Price_Predictor_WebApp
Stock Price Predictor App
# Overview
This project is a web application that predicts stock prices using historical data from Yahoo Finance. The app is built using Streamlit and employs an LSTM neural network model to forecast future prices. Users can visualize the stock's historical data, moving averages, and predicted prices.

# Features
Fetches historical stock data from Yahoo Finance.
Displays data visualization including adjusted close prices and moving averages.
Uses LSTM neural network for stock price prediction.
Interactive web interface for inputting stock ticker symbols and viewing predictions.
Visual comparison of original vs. predicted stock prices.

# Technical Details

# Data Collection:

Historical stock data is fetched using the yfinance library, which provides easy access to Yahoo Finance data.
The data spans 20 years from the current date, offering a comprehensive historical view for training the model.

# Data Preprocessing:

Missing values are handled and filled appropriately, ensuring a clean dataset for analysis.
The Adj Close price is used for predictions as it accounts for stock splits and dividend distributions, providing a more accurate representation than the Close price.

# Data Visualization:

The application uses matplotlib for plotting various graphs, such as the stock's adjusted closing prices and moving averages (100-day, 200-day, and 250-day).
Custom functions (plot_graph) are implemented to streamline the process of generating and displaying these plots in the app.

# Feature Engineering:

Moving Averages (MA) are calculated for 100, 200, and 250-day windows to identify long-term trends.
Percentage changes are computed to understand the day-to-day volatility and patterns in stock prices.

# Model Building:

The LSTM model is constructed using Keras, with layers configured to handle the sequential nature of stock data.
The model consists of two LSTM layers followed by dense layers, and it is compiled with the Adam optimizer and mean squared error loss function.
Training involves fitting the model to the training data with a batch size of 1 and 2 epochs, ensuring the model captures temporal dependencies effectively.

# Prediction and Inverse Scaling:

After training, the model is used to predict future stock prices based on the testing data.
Predicted values are inverse-transformed using the MinMaxScaler to revert them back to their original scale.

# Web Application:

The web app is developed using Streamlit, offering an interactive and easy-to-use interface.
Users can input a stock ticker symbol, and the app will fetch and display historical data, calculate moving averages, and predict future prices.
The app visually compares the original test data with predicted values, helping users to understand the model's performance.

# Deployment:

The trained model is saved and loaded in the Streamlit app to avoid retraining, speeding up the prediction process.
The app is designed to be deployed on platforms supporting Streamlit, making it accessible to a wide audience.


# How to Run

Clone the repository.
Install required packages:

pip install -r requirements.txt

Run the Streamlit app:

streamlit run web_stock_price_predictor.py

Usage
Enter the stock ticker symbol (e.g., GOOG) in the input box.
View the historical stock data and various moving averages.
Check the predicted stock prices and compare with the original data.


