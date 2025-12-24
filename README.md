# House Prices Prediction - Advanced Regression Techniques

This project aims to predict house prices using a **linear regression model with L2 regularization and early stopping**, applied to the "House Prices: Advanced Regression Techniques" dataset from Kaggle.  

---

## Overview

The goal of this project is to predict the sale price of houses based on various features such as lot area, year built, neighborhood, and more. The workflow includes:  

1. Data exploration and profiling  
2. Data cleaning and preprocessing  
3. Feature engineering  
4. Model training with linear regression, L2 regularization, and early stopping  
5. Validation and evaluation  
6. Submission file preparation for Kaggle  

---

## Dataset

- **Train dataset**: Contains features and the target variable `SalePrice`.  
- **Test dataset**: Contains only features (used for making predictions).  
- Source: [Kaggle - House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)  


---

## Data Exploration

- Used **pandas-profiling** for quick overview of the dataset.  
- Checked for missing values, duplicated rows, and uniform features.  
- Visualized relationships between features and the target variable.  

---

## Data Cleaning

- Dropped columns with too many missing values (`Alley`, `PoolQC`, `Fence`, `MiscFeature`)  
- Filled missing numeric features with mean and categorical features with mode  
- Removed duplicate rows  
- Dropped columns with uniform distribution  

---

## Feature Engineering

- **Season**: Derived from month sold (`MoSold`)  
- **HouseAge**: Calculated as `YrSold - YearBuilt`  
- Checked correlations of new features with the target variable  

---

## Data Preprocessing

- **Categorical Encoding**:  
  - Ordinal features → Label Encoding  
  - Nominal features → One-hot Encoding  
- **Feature Scaling**: Used `MinMaxScaler` for numerical features  
- **Normality Transformation**: Applied `Box-Cox` transformation to skewed numeric features  

---

## Model Training and Evaluation

- **Model**: Linear Regression with **L2 regularization (Ridge)**  
- **Training method**: Batch Gradient Descent  
- **Overfitting reduction**: L2 regularization + early stopping  
- **Hyperparameter tuning**: Tried different learning rates  
- **Train-validation split**: 80%-20%  

**Validation RMSE**: `0.04169`  

---

## Submission

- Processed test data same as training data  
- Predicted `SalePrice` for test data  
- Prepared `submission.csv` for Kaggle submission  
