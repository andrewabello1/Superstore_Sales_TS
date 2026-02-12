# Superstore_Sales_TS -  – ARIMA & Holt-Winters Sales Modeling

This project focuses on building, evaluating, and forecasting a monthly sales time series using classical forecasting techniques. The goal was to understand how different models capture **trend**, **seasonality**, and **noise**, and to compare model performance before generating future predictions.

---

## Project Overview

In this notebook, I applied two main forecasting approaches:

- **ARIMA / SARIMA** for statistical time-series modeling
- **Holt-Winters (Exponential Smoothing)** to capture level, trend, and seasonal patterns

The workflow includes:

1. Exploratory analysis and visualization of the time series  
2. Model fitting and comparison using fitted values  
3. Residual diagnostics to validate model assumptions  
4. Selection of the best model based on performance metrics  
5. Forecasting future periods (12-month horizon)

---

## Tools & Libraries

- `Python`
- `pandas`, `numpy`
- `matplotlib`
- `statsmodels`
  - `ExponentialSmoothing`
  - `seasonal_decompose`
- `sklearn.metrics`
  - `mean_squared_error`
  - `mean_absolute_error`

---

## Methodology

### ARIMA Modeling
- Checked stationarity and model assumptions
- Evaluated model fit using **fitted values**
- Generated forward forecasts

### Holt-Winters Modeling
Tested multiple configurations:
- Additive trend + additive seasonality
- Multiplicative seasonality
- Multiplicative trend

Each model was compared using:

- RMSE
- MAE

The best model was selected automatically and used to forecast future sales.

---

## Model Evaluation vs Forecasting

A key learning from this project is the difference between:

- **Model evaluation:** comparing fitted values against historical data
- **Forecasting:** predicting values beyond the last observed date

Residual analysis confirmed that the best model captured most of the structure in the data, leaving errors close to white noise.

---

## Results

- Identified the best Holt-Winters specification based on RMSE
- Generated a 12-month forward forecast
- Visualized fitted values, residuals, and future predictions

---

## Key Takeaways

- Holt-Winters models do not require strict stationarity like ARIMA.
- Multiplicative components help when variance increases over time.
- Residual analysis is critical to validate forecasting models.

---
