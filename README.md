# 📈 Stock Price Prediction using Time Series Analysis

This project focuses on analyzing and forecasting stock prices using historical data with time series techniques such as decomposition, stationarity checks, and transformation.

## 📊 Dataset

- **Columns**: Date, Open, High, Low, Close, Adj Close, Volume
- Sample: Daily stock prices from 2018-02-05 onwards

## 🧪 Project Steps

### 1. **Data Preprocessing**
- Selected the `Close` or `Adj Close` price as the `Final_Price` column
- Converted Date column to datetime format and set as index

### 2. **Seasonal Decomposition**
- Used `seasonal_decompose()` to analyze trend, seasonality, and residuals

### 3. **Stationarity Check**
- Applied Augmented Dickey-Fuller test (`adfuller()`)
- Used rolling mean and rolling std plots to visually check for stationarity

```python
rolling_mean = df['Final_Price'].rolling(window=3).mean()
rolling_std = df['Final_Price'].rolling(window=3).std()
