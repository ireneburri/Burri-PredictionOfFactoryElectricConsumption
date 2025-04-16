# Factory Electric Consumption Prediction

## Project Description
The notebook is structured into the following sections:

1. **Import Useful Libraries:** Import libraries listed in the prerequisites and set the random state.

2. **Load the Data and Print Statistics:** 
Load the train.csv file and visualize it using commands like head, info, and describe.

3. **Plot the Data:** Create visualizations to analyze the relationship between various features of the dataset and the target variable (Electric_Consumption), providing key insights and observations.

4. **Data Processing:** Remove outliers, extract features, handle missing values and drop useless columns
    - **Feature Extraction:** Extract information of time-based features such as "Hour", "DayOfWeek", "Month" and "Day" and drop "Date" column.
    - **Outliers Analysis:**  Analysis of the Outliers based on boxplots and distribution plots. Then clipping off the outliers from some features.
    - **Checks for missing values**
    - **Encoding of non-numerical features:** Cyclical Encoding of Hour, DayOfWeek, Month, Day.

5. **Models Training and Evalutaion:** Different models were tried: *Linear Regression*, *Polynomial Regression*, *Random Forest Regressor*, *XGBoost Regressor*. For each model it was performed:
    - **Cross-Validation RMSE**
    - Hyperparameters tuning using **GridSearchCV**
    - **Feature Importance analysis:** I also attempt to remove the less important features using different threshold but the RMSE always increased. 
    - **RMSE** on the validation set.
    - **Post-processing** to ensure predictions are non-negative (even if we have no explanation about the dataset and we can't be sure we can't have netaive value, I logically deduct it).

6. **Results and Comparison:** The best RSME score was performed by the XGBoost Regressor, 1.51. 

## Kaggle competition
  
This project is based on the Kaggle competition: https://www.kaggle.com/competitions/prediction-of-factory-electric-consumption/.

## Installation & Startup

Clone the repository: 
> git clone https://github.com/ireneburri/Burri-PredictionOfFactoryElectricConsumption.git

All dependencies are listed in the requirements.txt file:  
> pip install -r requirements.txt




