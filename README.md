# Prediction of Factory Electric Consumption

This repository contains a regression solution for the [Kaggle competition on Factory Electric Consumption](https://www.kaggle.com/competitions/prediction-of-factory-electric-consumption/). The goal is to accurately predict the electric power consumption of a factory using historical sensor and usage data.

## Project Objective
To develop a regression model capable of predicting future electric consumption in a factory environment based on various numerical and categorical features. Accurate predictions can assist in optimizing energy usage, reducing operational costs, and enhancing sustainability.

## Dataset Summary

- **Training Set:** ~13,800 records
- **Test Set:** ~2,160 records (target to predict)
- **Target Variable:** `Electric_Consumption`
- **Evaluation Metric:** RMSE (Root Mean Squared Error)

## Models Used

- **Linear Regression**
- **Polynomial Regression** (with hyperparameter tuning)
- **Random Forest Regressor** (with hyperparameter tuning)
- **XGBoost Regressor** (with hyperparameter tuning)

## Model Evaluation

Models were evaluated using cross-validation (CV) and validation set performance:

| Model                 | CV RMSE | Validation RMSE | Best Parameters |
|-----------------------|---------|-----------------|-----------------|
| Polynomial Regression | ...     | ...             | ...             |
| Random Forest         | ...     | ...             | ...             |
| XGBoost               | ...     | ...             | ...             |


## ⚙️ Techniques Applied

- Data preprocessing (handling missing values, encoding, scaling)
- Feature engineering
- Polynomial feature expansion
- GridSearchCV for hyperparameter tuning
- Feature importance analysis
- Clipping predictions to non-negative values



