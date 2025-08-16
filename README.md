# House Prices Regression Analysis

A machine learning project for predicting house sale prices using advanced regression techniques, created for the [Kaggle “House Prices – Advanced Regression Techniques” competition](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview).

---

## 🏠 Project Overview

The goal of this project was to build a regression model capable of accurately predicting the sale prices of homes in Ames, Iowa, based on a wide range of features such as square footage, neighborhood, and quality of materials.  

The challenge lies in handling missing data, engineering meaningful features, and leveraging powerful regression/ensemble models to reduce prediction error.

---

## 🔍 Analysis Workflow

### 1. Exploratory Data Analysis (EDA)
- Examined distributions and detected skewness in numerical features.  
- Analyzed categorical variables and their relationship with `SalePrice`.  
- Identified outliers and missing values.  

### 2. Data Cleaning & Preprocessing
- Imputed missing values using appropriate strategies (median, mode, or domain knowledge).  
- Handled categorical features using one-hot encoding and label encoding.  
- Applied log transformation to `SalePrice` to normalize skewness.  

### 3. Feature Engineering
- Created new features such as `TotalSF` (total square footage) and `TotalBath`.  
- Combined related variables to reduce redundancy.  
- Standardized/normalized numerical features for consistent scaling.  

### 4. Modeling
- Implemented and compared multiple regression models:  
  - Linear Regression, Ridge, Lasso  
  - Random Forest, Gradient Boosting, XGBoost, LightGBM  
- Used cross-validation (CV) to avoid overfitting and ensure robustness.  

### 5. Ensembling
- Blended top-performing models to leverage their strengths.  
- Stacking was used with a meta-model to minimize CV error.  

### 6. Evaluation & Submission
- Predictions were generated on the test dataset.  
- Applied `expm1` transformation to revert log-transformed predictions.  
- Created a valid `submission.csv` with `Id` and `SalePrice`.  

---

## 📊 Results

- **Public Kaggle Score (RMSLE): 0.12606**  
- Achieved through careful feature engineering, regularization, and ensembling.  
- Feature importance analysis showed that variables like *OverallQual, GrLivArea, TotalSF, GarageCars,* and *Neighborhood* were most influential in predicting sale price.  

---

## 🛠️ Tools & Libraries

- **Python**, **Jupyter Notebook**  
- **pandas, numpy** for data handling  
- **matplotlib, seaborn** for visualization  
- **scikit-learn** for preprocessing and regression models  
- **xgboost, lightgbm** for gradient boosting methods  

---

## 📌 Conclusion

This project demonstrates the complete lifecycle of a machine learning regression workflow—covering **EDA, data preprocessing, feature engineering, model training, and ensembling**—to achieve a competitive Kaggle score.  

The achieved **score of 0.12606** highlights the effectiveness of combining feature engineering with ensemble learning techniques in predictive modeling.  
