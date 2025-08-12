# ☕ Coffee Shop Sales Analysis & Forecasting

This project performs **Exploratory Data Analysis (EDA)**, **Time Series Forecasting**, and **Customer Insights** on coffee shop sales data.  
Using Python’s data analysis and statistical modeling libraries, the project identifies **sales trends**, **predicts future revenue**, and **highlights top customers**.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Analysis Steps](#analysis-steps)
- [Forecasting](#forecasting)
- [Customer Insights](#customer-insights)
- [Installation](#installation)
- [Usage](#usage)
- [Output](#output)
- [License](#license)

---

## 📖 Overview
The goal of this project is to:
1. Perform **time series EDA** on coffee sales.
2. Identify **monthly, weekly, and hourly sales patterns**.
3. Forecast **next week’s sales** using **Holt-Winters Exponential Smoothing**.
4. Analyze customer purchasing behavior.

---

## 📂 Dataset
The dataset (`index.csv`) contains:
- **Transaction details** (date, time, payment method, coffee type, sales amount)
- **Customer identifiers** (e.g., card IDs)
- **Monetary values** for sales analysis

---

## 🧾 Features
| Column Name   | Description |
|---------------|-------------|
| `date`        | Date of purchase |
| `datetime`    | Exact timestamp of purchase |
| `coffee_name` | Type of coffee sold |
| `money`       | Revenue from the sale |
| `card`        | Payment method or customer card ID |
| `...`         | Additional columns depending on dataset |

Engineered features:
- **`month`** → Extracted month-year (`YYYY-MM`)
- **`day`** → Day of the week (`0=Sunday` to `6=Saturday`)
- **`hour`** → Hour of the day (0–23)

---

## 📊 Analysis Steps

### 1️⃣ Time Series EDA
- **Monthly Sales Trends** → Line plots by coffee type
- **Weekly Sales Trends** → Bar plots by day of the week
- **Hourly Sales Trends** → Bar plots for peak hours

### 2️⃣ Forecasting (Next Week Sales)
- Aggregates daily sales revenue
- Fits a **Holt-Winters Exponential Smoothing** model with:
  - **Additive trend**
  - **Additive seasonality**
  - **7-day seasonal period**
- Forecasts **next 7 days** of sales

### 3️⃣ Customer Insights
- Groups customers by card ID
- Calculates:
  - **Total spending**
  - **Most purchased coffee**
- Ranks **Top 5 customers by total spending**

---

## 📈 Forecast Example
The forecasting step outputs:
- **Actual Sales** (historical data)
- **Fitted Sales** (model fit to past data)
- **Forecasted Sales** (next 7 days)
