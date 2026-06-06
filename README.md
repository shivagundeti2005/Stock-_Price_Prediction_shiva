# Stock-_Price_Prediction_shiva
📈 Stock Price Prediction using Time Series Forecasting

A machine learning and time-series analysis project for forecasting Tata Global Beverages stock prices using historical NSE stock market data. This project explores data preprocessing, stationarity testing, trend decomposition, and multiple forecasting techniques including Moving Average, Auto ARIMA, and SARIMA models.

 🚀 Project Overview

This notebook performs:

- Historical stock data analysis
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Stationarity testing using Augmented Dickey-Fuller (ADF) Test
- Time-series decomposition
- Forecasting using:
  - Moving Average
  - Auto ARIMA
  - SARIMA
- Model evaluation using RMSE

The dataset contains historical stock prices of Tata Global Beverages listed on the National Stock Exchange (NSE).

---

 📂 Dataset

**File:** `NSE-TATAGLOBAL.csv`

 Features

| Column | Description |
|----------|-------------|
| Date | Trading Date |
| Open | Opening Price |
| High | Highest Price |
| Low | Lowest Price |
| Last | Last Traded Price |
| Close | Closing Price |
| Total Trade Quantity | Total Volume Traded |
| Turnover (Lacs) | Daily Turnover |

**Dataset Size:** 2,035 records

---
 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- pmdarima
- Prophet
- Scikit-learn

---
 📦 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/stock-price-prediction.git
cd stock-price-prediction
```

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn
pip install statsmodels pmdarima prophet scikit-learn
```

---
 📊 Workflow

 1. Data Preprocessing

- Load stock market dataset
- Convert Date column to datetime format
- Reverse chronological order
- Handle duplicates and missing values
- Set Date as index

 2. Exploratory Data Analysis

Visualize:

- Open Price
- High Price
- Low Price
- Close Price
- Trading Volume

Identify:

- Trends
- Seasonality
- Market behavior

 3. Stationarity Testing

Augmented Dickey-Fuller (ADF) Test is used to determine whether the time series is stationary.

```python
adfuller(series)
```

 4. Time Series Decomposition

Separate the series into:

- Trend
- Seasonality
- Residual Components

```python
seasonal_decompose(data['Open'])
```

 5. Forecasting Models

 Moving Average Model

Simple baseline forecasting model using historical averages.

Auto ARIMA

Automatically identifies optimal ARIMA parameters.

```python
auto_arima(
    training,
    seasonal=True,
    d=1,
    D=1
)
```

SARIMA

Seasonal AutoRegressive Integrated Moving Average model for capturing seasonality.

```python
SARIMAX(
    training,
    order=(1,1,1),
    seasonal_order=(1,1,1,12)
)
```

---

 📈 Evaluation Metric

Root Mean Square Error (RMSE)

```python
rmse = np.sqrt(mean_squared_error(actual, predicted))
```

Lower RMSE indicates better forecasting performance.

---

 📷 Sample Visualizations

- Stock Price Trends
- Rolling Mean & Standard Deviation
- Seasonal Decomposition
- Actual vs Predicted Stock Prices

---

 📁 Project Structure

```text
stock-price-prediction/
│
├── NSE-TATAGLOBAL.csv
├── stock-price-prediction.ipynb
├── README.md
│
└── outputs/
    ├── trend_analysis.png
    ├── decomposition.png
    └── forecast_results.png
```

---

## 🎯 Future Improvements

- Implement LSTM Deep Learning models
- Add XGBoost-based forecasting
- Hyperparameter tuning
- Real-time stock prediction pipeline
- Deploy as a web application using Streamlit

---

 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature-name
```

3. Commit changes

```bash
git commit -m "Add new feature"
```

4. Push to GitHub

```bash
git push origin feature-name
```

5. Open a Pull Request

---

 📜 License

This project is licensed under the MIT License.

---

 👨‍💻 Author

Shivakumar Gundeti

GitHub: https://github.com/yourusername
