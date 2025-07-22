# 🚑 ER Wait Time Forecasting

Forecasting daily EMS (Emergency Medical Services) dispatch response times using real-world NYC data and machine learning.

This project demonstrates how time series features and XGBoost regression can be used to model and predict emergency response trends.

---

## 📌 Project Overview

- **Goal:** Predict the average EMS dispatch response time per day using historical patterns.
- **Data:** EMS Incident Dispatch Data from [NYC Open Data](https://data.cityofnewyork.us/Public-Safety/EMS-Incident-Dispatch-Data/76xm-jjuj).
- **Tech stack:** Python, Pandas, XGBoost, Matplotlib, scikit-learn

---

## 🔍 Problem Context

EMS response times can be impacted by trends like:
- Day of the week
- Past delays (lag)
- Recent spikes or dips (rolling averages)

Predicting these times can help cities better allocate resources and identify potential systemic bottlenecks.

---

## 🧪 Features Engineered

| Feature Type     | Examples                          | Description |
|------------------|------------------------------------|-------------|
| Time-based       | `day_of_week`, `is_weekend`        | Captures weekly patterns |
| Lag features     | `lag_1`, `lag_7`                   | Yesterday’s and last week’s response time |
| Rolling averages | `rolling_7`, `rolling_14`          | 7- and 14-day moving averages to smooth trends |

---

## ⚙️ Model

- **Model:** `XGBRegressor`
- **Train/Test Split:** Trained on data before 2023; tested on 2023–2024
- **Metrics:**
  - **RMSE:** ~617 seconds
  - **MAE:** ~308 seconds

---
