# Multi-Stock Analysis & Price Prediction: LSTM vs. ARIMA

## 📌 Project Overview
This project demonstrates an end-to-end data science workflow applied to financial stock markets. It includes comprehensive **Exploratory Data Analysis (EDA)** of a diversified portfolio and advanced **Time Series Forecasting** to predict future stock prices.

The core focus is a comparative study between two methodologies:

- **LSTM (Long Short-Term Memory):** A deep learning recurrent neural network designed to capture non-linear dependencies.  
- **ARIMA (AutoRegressive Integrated Moving Average):** A classical statistical model focused on trend stationarity and autocorrelations.

---

## 📊 Key Research Questions
This analysis aims to answer the following:

1. How did stock prices change over time?  
2. What were the moving averages for various stocks?  
3. What was the average daily return?  
4. How correlated are different stocks?  
5. How much value is at risk (VaR) for a particular investment?  
6. Can we predict future stock behavior (Apple Inc.)?  
7. Which model (LSTM vs. ARIMA) performs better?

---

## 🛠️ Tech Stack
- **Data Source:** [yfinance](https://pypi.org/project/yfinance/) (Yahoo Finance API)  
- **Analysis:** Pandas, NumPy  
- **Visualization:** Matplotlib, Seaborn  
- **Machine Learning:** TensorFlow/Keras (LSTM)  
- **Statistical Modeling:** statsmodels, pmdarima (Auto-ARIMA)  

---

## 📈 Methodology & Results

### 1. Data Collection
Historical stock data was pulled for:
- Apple (AAPL)  
- Tesla (TSLA)  
- Coca-Cola (KO)  
- Booking Holdings (BKNG)

### 2. Risk Analysis
Risk metrics were calculated using **Monte Carlo simulations** and **Bootstrap methods** to determine the **Value at Risk (VaR)**.

### 3. Forecasting Apple (AAPL) Closing Prices
- **LSTM Model:** Configured with 50-unit layers and trained over 1 epoch (demo purposes).  
  - **RMSE:** 8.29  

- **ARIMA Model:** Utilized `auto_arima` after confirming non-stationarity with the Augmented Dickey-Fuller (ADF) test.  
  - **RMSE:** 4.09  

**Conclusion:** ARIMA outperformed LSTM in this scenario, highlighting that traditional statistical models can be more robust than deep learning for highly volatile financial time series.

---

## 🏆 Final Metrics
| Model | RMSE |
|-------|------|
| ARIMA | 4.09 |
| LSTM  | 8.29 |

---

## 🚀 How to Use
1. Clone the repository:
```bash
git clone <your-repo-url>
