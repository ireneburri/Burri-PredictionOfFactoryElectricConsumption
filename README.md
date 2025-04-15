# Prediction of Factory Electric Consumption

This repository contains a regression solution for the [Kaggle competition on Factory Electric Consumption](https://www.kaggle.com/competitions/prediction-of-factory-electric-consumption/). The goal is to accurately predict the electric power consumption of a factory using historical sensor and usage data.

## Project Objective
To develop a regression model capable of predicting future electric consumption in a factory environment based on various numerical and categorical features. Accurate predictions can assist in optimizing energy usage, reducing operational costs, and enhancing sustainability.

## Dataset Summary

- **Training Set:** 13 872 records
- **Test Set:** 2 160 records (target to predict)
- **Target Variable:** `Electric_Consumption`
- **Evaluation Metric:** RMSE (Root Mean Squared Error)

## Models Used

- **Linear Regression**
- **Polynomial Regression** (with hyperparameter tuning)
- **Random Forest Regressor** (with hyperparameter tuning)
- **XGBoost Regressor** (with hyperparameter tuning)

## Model Evaluation

Models were evaluated using cross-validation (CV) and validation set performance:

| Model                 | CV RMSE     | Validation RMSE | Best Parameters           |
|-----------------------|-------------|-----------------|---------------------------|
| Polynomial Regression | 3.99 ± 0.60 | 2.463049        | {'degree': 3,'include_bias': False}   |
| Random Forest         | 2.60 ± 0.55 | 1.630461        | {'max_depth': None,'min_samples_split': 2,'n_estimators': 200}     |
| XGBoost               | 2.68 ± 0.49 | 1.48319         | {'learning_rate': 0.05, 'max_depth': 8, 'n_estimators': 1000, 'subsample': 0.8 }       |

## Techniques Applied

- Data preprocessing (handling missing values, encoding, scaling)
- Feature engineering
- Polynomial feature expansion
- GridSearchCV for hyperparameter tuning
- Feature importance analysis
- Clipping predictions to non-negative values

## 🛠 Tools & Libraries

- Python 3.9+
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- xgboost
- joblib

## References

- [Kaggle Competition](https://www.kaggle.com/competitions/prediction-of-factory-electric-consumption/)
- [Scikit-learn](https://scikit-learn.org/)
- [XGBoost](https://xgboost.readthedocs.io/)

## Contents

- **delivery/** – Contains the complete solution:
  - Python Notebook (`.ipynb`)
  - PDF export of the notebook (landscape format)
  - Setup instructions and environment requirements
- **data/** – Includes training and test data 
- **README.md** – Project overview, objectives, and references
