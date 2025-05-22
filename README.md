# Baltimore-AQI-predications-using-Regressors
#  Predicting Air Quality Index (AQI) in Baltimore using regressors and extreme value theory. Combines ML models (XGBoost, RF, LSTM) with statistical modeling (GEV/GPD) for accurate extreme event forecasting.

This repository presents our final project for DATA 602 (Data Mining & Machine Learning for Business) at UMBC. The objective is to build robust machine learning models to predict daily **Air Quality Index (AQI)** in **Baltimore City** and accurately capture **extreme pollution events** using **Extreme Value Theory (EVT)**.

## 📌 Objective

- Predict daily AQI using ML models (Linear Regression, XGBoost, Random Forest, LSTM)
- Identify and forecast **extreme AQI values** using **Peak-Over-Threshold (POT)** and **Block Maxima** methods
- Integrate Extreme Value Theory (GEV & GPD) with ML for hybrid modeling

## 🧠 Methodology Overview

### 🔍 Machine Learning Models
- Linear Regression, Lasso, Ridge, Bayesian Ridge
- Random Forest Regressor (Best Tree-based Model)
- XGBoost (Best overall)
- KNN, AdaBoost (Baseline comparisons)
- LSTM (for time-series dependency)

### 📈 Evaluation Metrics
- RMSE (Root Mean Square Error)
- R² Score (Explained Variance)

### 📊 Extreme Value Theory
- Block Maxima using GEV Distribution
- Peak Over Threshold using GPD
- Tail modeling for AQI > 150

## 📂 Dataset

- Source: [U.S. EPA AirData](https://www.epa.gov/outdoor-air-quality-data)
- Location: Baltimore City, Maryland
- Time Span: 2006–2023
- Features: AQI, PM2.5, PM10, NO₂, SO₂, CO, Ozone, Temperature, Wind, Pressure

## 💡 Key Insights

- PM2.5 and Ozone are the strongest predictors of AQI.
- XGBoost and Random Forest achieve **R² ~0.85** with RMSE ~9.
- EVT + ML hybrid models can estimate **probability of future extreme events**.
- POT with GPD offers more precise modeling than Block Maxima.

## 🧪 Results Summary

| Model              | Test RMSE | Test R²  |
|-------------------|-----------|----------|
| Random Forest      | 8.9       | 0.86     |
| XGBoost            | 9.09      | 0.85     |
| LSTM               | 8.99      | 0.85     |
| XGBoost + EVT      | 11.0      | 0.82     |
| RF + EVT           | 10.5      | 0.83     |

## 📁 Files

- `DATA 602 Group3 Final Project Notebook.ipynb`: Full code and model evaluations
- `DATA 602 FINAL.pptx`: Presentation deck summarizing findings and methodology

## 👥 Team Members

- Daniel McKirgan  
- Naga Sai Kartikeya Vemula  
- Amisha Ganvir  
- Tanmay Pendharkar  

## 🔮 Future Work

- Implement **rolling window** EVT prediction for dynamic thresholding
- Incorporate **real-time traffic and port data** for improved accuracy
- Deploy models as **public-facing tools** for government agencies

