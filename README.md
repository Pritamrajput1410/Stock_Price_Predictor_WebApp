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

Data Collection: Utilizes yfinance to fetch historical stock data.

Preprocessing: Handles missing values, uses adjusted close prices.

Feature Engineering: Calculates moving averages (100, 200, 250 days) and percentage changes.

Model: LSTM neural network built with Keras.

Visualization: Uses matplotlib for plotting graphs.

Web App: Developed with Streamlit for an interactive user interface.

Deployment: Model saved and loaded for fast predictions.


# How to Run

Clone the repository.
Install required packages:

pip install -r requirements.txt

Run the Streamlit app:

streamlit run app.py

Usage
Enter the stock ticker symbol (e.g., GOOG) in the input box.
View the historical stock data and various moving averages.
Check the predicted stock prices and compare with the original data.


