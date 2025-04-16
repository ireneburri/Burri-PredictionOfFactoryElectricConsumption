# Prediction of Factory Electric Consumption

This repository contains a regression solution for the [Kaggle competition on Factory Electric Consumption](https://www.kaggle.com/competitions/prediction-of-factory-electric-consumption/). The goal is to accurately predict the electric power consumption of a factory using historical sensor and usage data.

## Project Objective
To develop a regression model capable of predicting future electric consumption in a factory environment based on various numerical and categorical features. Accurate predictions can assist in optimizing energy usage, reducing operational costs, and enhancing sustainability.

## Dataset Summary

- **Training Set:** 13 872 records
- **Test Set:** 2 160 records (target to predict)
- **Target Variable:** Electric_Consumption
- **Evaluation Metric:** RMSE (Root Mean Squared Error)

## Models Used

- **Linear Regression**
- **Polynomial Regression** (with hyperparameter tuning)
- **Random Forest Regressor** (with hyperparameter tuning)
- **XGBoost Regressor** (with hyperparameter tuning)

## Project Structure

- **Libraries Used**
- **Data Visualization and Exploration**
- **Data Processing:**
    - **Feature Extraction** 
    - **Outliers Analysis** 
    - **Checks for missing values**
    - **Encoding of non-numerical features** 
- **Models Training and Evalutaion:** Different models were tried: *Linear Regression*, *Polynomial Regression*, *Random Forest Regressor*, *XGBoost Regressor*. For each model it was performed:
  - **Cross-Validation RMSE**
  - Hyperparameters tuning using **GridSearchCV**
  - **Feature Importance analysis**
  - **RMSE** on the validation set
  - **Post-processing** to ensure predictions are non-negative
- **Results and Comparison**

## Model Evaluation

Models were evaluated using cross-validation (CV) and validation set performance:

| Model                 | CV RMSE   | Std. Dev. | Validation RMSE | Best Parameters |
|-----------------------|-----------|-----------|------------------|-----------------|
| Linear Regression     | 3.476     | 0.199     | 3.192            | Default |
| Polynomial Regression | 3.064     | 1.112     | 2.241            | `{'polynomialfeatures__degree': 2, 'polynomialfeatures__include_bias': True}` |
| Random Forest         | 2.434     | 0.450     | 1.674            | `{'max_depth': None, 'min_samples_split': 2, 'n_estimators': 200}` |
| XGBoost               | 2.520     | 0.430     | **1.494**        | `{'learning_rate': 0.05, 'max_depth': 6, 'n_estimators': 1000, 'predictor': 'cpu_predictor', 'subsample': 0.8, 'tree_method': 'hist'}` |


## References

- [Kaggle Competition](https://www.kaggle.com/competitions/prediction-of-factory-electric-consumption/)

## Contents

- **Software_and_Data/** – Contains the complete solution:
  - Python Notebook (`.ipynb` and `.pdf`)
  - Setup instructions and environment requirements
  - **Data/** – Includes training, test data and a submission folder with the different predictions
  - **README.md** – Project description
- **Doc/** - Contains:
  - Slides for the presentation (`.tex` and `.pdf`)
- **README.md** – Project overview
