# Retail Demand Forecasting with LightGBM
Project Overview: This repository contains a high-performance predictive pipeline for retail demand forecasting. Using a LightGBM Regressor, the model analyzes over 1 million records to predict daily sales across 12 stores and 50 different items.The core of this project focuses on Feature Engineering, specifically leveraging time-series lag variables to capture seasonal trends and recent consumer behavior.
# Dataset Highlights
The model was trained on a comprehensive retail dataset with the following characteristics:
Volume: 1,048,575 rows.
Features: date, store_id, item_id, price, and promo.Target: sales (Daily volume).
Granularity: 12 unique stores and 50 unique items.⚙️ Technical Workflow1.
Feature Engineering: To turn static retail data into a time-series powerhouse, the following features were engineered.
Temporal Features: Extracted day, week, and year from the date.Lag Features: Created lag_1 (previous day), lag_7 (same day last week), and lag_30 (last month) to provide the model with historical context.
Strategy Algorithm: LightGBM (Gradient Boosting Machine).
Validation: Time-based split to ensure the model generalizes to future dates.
Optimization: Categorical features (store_id, item_id) were handled via label encoding or internal LightGBM optimization.
Performance Metrics: 
MAE (Mean Absolute Error): 2.62
RMSE (Root Mean Squared Error): 3.29'
SMAPE (Symmetric Mean Absolute Percentage Error): 10.27%
