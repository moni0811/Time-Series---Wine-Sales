# 📈 Time Series Forecasting of Sparkling Wine Sales

This repository contains a time series forecasting analysis of Sparkling Wine sales. The project aims to uncover historical trends and seasonality in the data and forecast future sales to support better business decisions around planning and inventory.

---

## 🧠 Objective

The purpose of this analysis is to:

- Understand underlying trends and seasonality in Sparkling Wine sales
- Evaluate multiple forecasting models using historical data
- Identify the most accurate model based on RMSE performance
- Generate a 12-month forecast using the selected model

---

## 📂 What's in the Repo

- `sparkling_time_series.py` – Python script with the complete analysis and modeling pipeline
- `README.md` – This file

> **Note:** The sales dataset (`Sparkling.csv`) is **confidential** and **not included** in this repository. For internal use, ensure the file is placed in the project root before running the script.

---

## 🛠 Methods Used

The workflow includes:

1. **Time Series Preparation & Visualization**
   - Line plots, boxplots, and decomposition (additive & multiplicative)

2. **Train/Test Split**
   - Training: Data before 1991
   - Testing: Data from 1991 onward

3. **Forecasting Models Built**
   - Linear Regression
   - Naïve Forecast
   - Simple Average
   - Simple Exponential Smoothing
   - Double Exponential Smoothing (Holt’s Method)
   - Triple Exponential Smoothing:
     - Additive
     - Multiplicative
     - Hybrid (Additive trend + Multiplicative seasonality)

4. **Evaluation**
   - RMSE calculated on test data for all models
   - Results summarized in a comparative table

5. **Forecasting**
   - Best-performing model retrained on full dataset
   - Forecast generated for the next 12 months

---

## 🔍 Results Summary

The data shows consistent **seasonal behavior** and an **upward trend**. Among the models tested, the **Triple Exponential Smoothing** model (Additive trend + Multiplicative seasonality) yielded the most accurate results.

| Model                                            | Test RMSE |
|--------------------------------------------------|-----------|
| Linear Regression                                | 1389.13   |
| Naïve Forecast                                   | 3864.27   |
| Simple Average                                   | 1275.08   |
| Simple Exponential Smoothing                     | 1338.00   |
| Double Exponential Smoothing                     | 5291.87   |
| TES (Additive)                                   | 378.62    |
| TES (Multiplicative)                             | 380.39    |
| **TES (Additive + Multiplicative)**              | 317.43 ✅ Lowest |

---

## 📅 Forecast Insights

- 12-month forecast generated using the optimal model
- Useful for planning procurement, marketing, and budgeting aligned with seasonal patterns

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/moni0811/Time-Series---Wine-Sales.git
   cd sparkling_wine_forecasting
2. Install below requirements if not installed
   pip install pandas numpy matplotlib seaborn statsmodels scikit-learn
3. Run your analysis script
   python sparkling_time_series.py
