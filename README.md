Multi-Stock Analysis & Price Prediction: LSTM vs. ARIMA
📌 Project Overview
This project presents an end-to-end data science workflow applied to financial stock markets. It begins with a comprehensive Exploratory Data Analysis (EDA) of a diversified portfolio and moves into advanced Time Series Forecasting to predict future stock prices.

The core of the project is a comparative study between two distinct methodologies:

LSTM (Long Short-Term Memory): A deep learning recurrent neural network designed to capture non-linear dependencies.

ARIMA (AutoRegressive Integrated Moving Average): A classical statistical model focused on trend stationarity and autocorrelations.

📊 Key Research Questions
The analysis seeks to answer seven critical financial questions:

What was the change in stock price over time?

What were the moving averages for various stocks?

What was the average daily return?

What is the correlation between different stocks?

How much value is at risk (VaR) for a particular investment?

Can we predict future stock behavior (Apple Inc.)?

Which model (LSTM vs. ARIMA) performs better?

🛠️ Tech Stack
Data Source: yfinance (Yahoo Finance API)

Analysis: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: TensorFlow/Keras (LSTM)

Statistical Modeling: statsmodels, pmdarima (Auto-ARIMA)

📈 Methodology & Results
1. Data Collection
Historical data was pulled for Apple (AAPL), Tesla (TSLA), Coca-Cola (KO), and Booking Holdings (BKNG).

2. Risk Analysis
The project calculates risk using Monte Carlo simulations and the Bootstrap method to determine the Value at Risk (VaR).

3. Forecasting Apple (AAPL) Closing Prices
LSTM Model: Configured with 50-unit layers and trained over 1 epoch (for demonstration). It achieved an RMSE of 8.29.

ARIMA Model: Utilizing auto_arima after verifying non-stationarity via the Augmented Dickey-Fuller (ADF) test. It achieved a significantly lower RMSE of 4.09.

🏆 Final Conclusion
Contrary to the common assumption that Deep Learning is always superior, the ARIMA model outperformed the LSTM model in this specific scenario.

ARIMA RMSE: 4.09

LSTM RMSE: 8.29

This highlights the importance of choosing the right tool for the data; in highly volatile financial time series, traditional statistical models that account for mean reversion and trends can sometimes be more robust than complex neural networks.

🚀 How to Use
Clone the repository.

Install dependencies: pip install yfinance pandas numpy matplotlib seaborn tensorflow pmdarima.

Run the Jupyter Notebook to see the step-by-step analysis and model comparisons.
