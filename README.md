# Stock Price Prediction: Opening Price Forecasting

This repository contains a Python-based project focused on predicting stock opening prices using historical stock data and macroeconomic indicators. The project experiments with various machine learning and deep learning techniques to model the data, evaluates their performance, and visualizes the results.

## Problem Statement

The goal is to predict the **opening price** of a stock based on the following features:
- **Historical Stock Data**: Opening price, closing price, and trading volume from previous days.
- **Industry Type**: Categorical variable representing the stock's industry (e.g., Technology for Tesla and Apple).
- **Time of Year**: Temporal features (e.g., day, month).
- **Macroeconomic Indicators**: Self-selected metrics such as Consumer Price Index (CPI), Producer Price Index (PPI), Unemployment Rate, and GDP from the Federal Reserve Economic Data (FRED) API.

## Datasets

### 1. Stock Price Data
- **Tesla Stock Data**: [Tesla Stock Data Updated Till 28-Jun-2021](https://www.kaggle.com/datasets/varpit94/tesla-stock-data-updated-till-28jun2021)
  - Features: Date, Open, High, Low, Close, Adjusted Close, Volume
  - Industry: Technology (Electric Vehicles)
- **Apple Stock Data**: [Apple Stock Data Updated Till 22-Jun-2021](https://www.kaggle.com/datasets/varpit94/apple-stock-data-updated-till-22jun2021)
  - Features: Date, Open, High, Low, Close, Adjusted Close, Volume
  - Industry: Technology (Consumer Electronics)

### 2. Macroeconomic Data
- **Source**: Federal Reserve Economic Data (FRED) API
- **Indicators**:
  - **CPIAUCSL**: Consumer Price Index for All Urban Consumers
  - **PPIACO**: Producer Price Index by Commodity
  - **UNRATE**: Unemployment Rate
  - **GDP**: Gross Domestic Product
- Accessed via: `fredapi` with an API key

## Tasks Performed

1. **Data Preprocessing**:
   - Merge stock data with macroeconomic indicators by date.
   - Extract temporal features (e.g., day, month) from the date.
   - Normalize numerical features using MinMaxScaler.
   - Handle missing data (e.g., GDP NaN values) with interpolation.

2. **Modeling Techniques**:
   - **Feedforward Neural Network (FNN)**: Multi-layer perceptron for static feature modeling.
   - **Recurrent Neural Network (RNN)**: Simple RNN and LSTM for capturing temporal dependencies.
   - **Traditional Algorithms**:
     - Linear Regression
     - Support Vector Machine (SVM) with SVR
     - Decision Tree Regressor
     - Random Forest Regressor

3. **Overfitting Prevention**:
   - Techniques: Early stopping, dropout layers (for neural networks), regularization (e.g., Ridge for Linear Regression), cross-validation.
   - Training graphs plotted (e.g., loss vs. epochs).

4. **Evaluation**:
   - Metrics: Mean Squared Error (MSE), Mean Absolute Error (MAE).
   - Comparison of model performance across methods.

5. **Visualization**:
   - Training/validation loss curves.
   - Predicted vs. actual opening prices.
   - Model comparison plots (e.g., bar charts of MSE).
   - Visualize Predictions for the best model (Linear Regression)

![image](https://github.com/user-attachments/assets/db5e5208-dcf3-4da5-9640-2cc81fb08821)
