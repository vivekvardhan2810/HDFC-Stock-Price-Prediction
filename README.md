# HDFC Stock Price Prediction using ARIMA and XGBoost

This project predicts the stock price of HDFC Bank using two models: ARIMA (Auto-Regressive Integrated Moving Average) and XGBoost (Extreme Gradient Boosting). The dataset contains historical stock prices, and we perform the following tasks:
- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Training the ARIMA model
- Training the XGBoost model
- Evaluation and forecasting of future stock prices

## Project Structure

```
├── HDFCBANK.NS.csv          # Dataset file
├── stock_prediction.ipynb   # Jupyter Notebook containing the code
└── README.md                # This README file
```

## Requirements

To run this project, you need the following libraries:

```
pip install pandas numpy matplotlib seaborn statsmodels xgboost scikit-learn
```

## Dataset

The dataset used in this project is ```HDFCBANK.NS.csv```, which contains the following columns:

- **Date**: Date of stock data

- **Open**: Opening price

- **High**: Highest price during the day

- **Low**: Lowest price during the day

- **Close**: Closing price at the end of the day

- **Volume**: Number of shares traded

- **Adj Close**: Adjusted closing price

## Steps

## 1. Exploratory Data Analysis (EDA)

We start by loading the dataset and visualizing the closing prices over time. We also check for any missing values and handle them.

## 2. ARIMA Model

**2.1 Preprocessing for ARIMA**

The time series data is differenced to make it stationary, and the data is split into training and testing sets.

**2.2 Training the ARIMA Model**

We fit the ARIMA model on the training data and print the model summary.

**2.3 Forecasting and Evaluation**

The model is used to forecast future stock prices, and we evaluate the performance using Mean Squared Error (MSE) and Mean Absolute Error (MAE).

## 3. XGBoost Model

**3.1 Preprocessing for XGBoost**

For XGBoost, we create features like Year, Month, Day, DayOfWeek, etc., and split the dataset into training and testing sets.

**3.2 Training the XGBoost Model**

We train the XGBoost model on the features and target (closing price).

**3.3 Forecasting and Evaluation**

The model is used to predict stock prices, and the performance is evaluated using MSE and MAE.

## Conclusion

Both models are trained on HDFC Bank stock price data. ARIMA is suitable for time series forecasting, while XGBoost utilizes feature engineering to predict stock prices. Based on the evaluation metrics, you can select the model that best suits your needs.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
