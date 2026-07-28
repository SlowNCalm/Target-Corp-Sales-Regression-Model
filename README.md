# Target-Corp-Sales-Regression-Model

This notebook aims to develop a regression model to forecast quarterly sales for Target Corporation. The analysis involves several key steps:

Data Loading and Initial Exploration: Loading historical quarterly sales data for Target Corp and visualizing the sales trends over time.
Feature Engineering: Creating a 'time' variable as an independent variable and a dummy variable to capture seasonality (specifically, the 4th quarter holiday shopping effect) along with an interaction term.
Model Training: Splitting the data into training and testing sets (75:25 split) and training an Ordinary Least Squares (OLS) regression model using statsmodels.
Prediction and Evaluation: Making predictions on the test set and generating prediction intervals with a specified confidence level.
Forecasting with External Data: Loading a separate forecast dataset and using the trained model to predict future sales.
