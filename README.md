# 📈 Target Corp Quarterly Sales Forecasting

A regression-based forecasting model that predicts Target Corporation's quarterly sales using historical trends and seasonal (holiday quarter) effects.

---

## 🧭 Overview

Retail sales are highly seasonal — especially around the Q4 holiday shopping season. This project builds an **Ordinary Least Squares (OLS) regression model** to forecast Target Corp's quarterly sales by capturing both the long-term trend and the recurring seasonal boost.

The notebook walks through the full workflow: loading and exploring historical sales data, engineering time and seasonality features, training and evaluating the model, and finally generating forward-looking forecasts on new data.

---

## 🎯 Project Goals

- Model the underlying trend in Target's quarterly sales over time
- Quantify the seasonal impact of the Q4 holiday shopping period
- Evaluate model performance with prediction intervals, not just point estimates
- Apply the trained model to forecast sales for future/unseen quarters

---

## 🛠️ Methodology

The analysis follows five main stages:

### 1. Data Loading & Initial Exploration
Historical quarterly sales data for Target Corp is loaded and visualized to identify overall trends, seasonality, and any irregularities in the data.

### 2. Feature Engineering
Two key features are engineered to feed the regression model:
- **`time`** — a numeric index representing the sequential progression of quarters (captures the long-term trend)
- **`Q4 dummy`** — a binary variable flagging the 4th-quarter holiday shopping season
- **Interaction term** — `time × Q4 dummy`, allowing the trend's slope to shift specifically during holiday quarters

### 3. Model Training
The dataset is split into **training (75%) and testing (25%)** sets. An **OLS regression model** is trained using `statsmodels` on the engineered features.

### 4. Prediction & Evaluation
The trained model generates predictions on the held-out test set, along with **prediction intervals** at a specified confidence level to quantify forecast uncertainty — not just single-point estimates.

### 5. Forecasting with External Data
A separate forecast dataset (future quarters) is loaded, and the trained model is applied to generate out-of-sample sales forecasts.

---

## 📦 Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| `pandas` | Data loading & manipulation |
| `statsmodels` | OLS regression modeling |
| `matplotlib` / `seaborn` | Data visualization |
| Jupyter Notebook | Analysis environment |

---

## 📊 Results

> *Add a short summary here once finalized — e.g. model R², key coefficients, and a chart of actual vs. predicted sales. A visual is worth including for anyone skimming the repo.*

---

## 🔮 Future Improvements

- Incorporate additional macroeconomic indicators (e.g. consumer spending index, inflation)
- Compare OLS performance against time-series models (ARIMA, Prophet)
- Automate quarterly data refresh via API pull

---

## 🤝 About This Project

This project was built as a hands-on exploration of regression-based forecasting applied to real-world retail sales data. Feedback and suggestions are welcome — feel free to open an issue or reach out!
