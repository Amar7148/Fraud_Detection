# 🚨 Fraud Detection on Financial Transactions  

## 📌 Project Overview  
This project implements an **end-to-end fraud detection pipeline** on a large-scale financial transactions dataset (**6.3M+ rows**). The goal is to proactively identify fraudulent transactions using **machine learning** while addressing **real-world challenges** such as data imbalance, multicollinearity, and feature engineering.  

## 🛠️ Key Features  
- **Exploratory Data Analysis (EDA)**  
  - Transaction type distribution, fraud ratio by type  
  - Fraud trends across time and transaction amount distribution  

- **Data Preprocessing**  
  - Handling missing values & multicollinearity  
  - Derived features:  
    - `origin_diff` = `oldbalanceOrg - newbalanceOrig`  
    - `dest_diff` = `newbalanceDest - oldbalanceDest`  
  - Dropped redundant balance columns  
  - Label encoding for categorical variables  
  - Standardization of numerical features  

- **Imbalanced Data Handling**  
  - Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance fraud vs non-fraud transactions  

- **Models Implemented**  
  - Logistic Regression  
  - Decision Tree  
  - Random Forest  
  - Naive Bayes  
  - XGBoost  
  - LightGBM  
  - CatBoost  

- **Evaluation Metrics**  
  - Accuracy, Precision, Recall, F1-score  
  - ROC-AUC, PR-AUC  
  - Confusion Matrix  
  - Matthews Correlation Coefficient (MCC)  

## 📊 Results  
| Model              | Accuracy | Precision | Recall | F1-score | ROC-AUC | PR-AUC | MCC   |  
|---------------------|----------|-----------|--------|----------|---------|--------|-------|  
| **Random Forest**   | 0.9993   | 0.65      | 0.94   | 0.77     | 0.9967  | 0.9390 | 0.78  |  
| **XGBoost**         | 0.9986   | 0.47      | 0.98   | 0.64     | 0.9996  | 0.9525 | 0.56  |  
| **LightGBM**        | 0.9978   | 0.37      | 0.99   | 0.54     | 0.9994  | 0.9537 | 0.57  |  
| Decision Tree       | 0.9990   | 0.58      | 0.89   | 0.70     | 0.9440  | 0.7364 | 0.72  |  
| CatBoost            | 0.9963   | 0.26      | 0.99   | 0.41     | 0.9960  | 0.9414 | 0.50  |  
| Naive Bayes         | 0.9950   | 0.12      | 0.45   | 0.19     | 0.9153  | 0.2327 | 0.23  |  
| Logistic Regression | 0.9682   | 0.04      | 0.93   | 0.07     | 0.9879  | 0.6293 | 0.18  |  

✅ **Best balance of Recall and Precision:** XGBoost & LightGBM  
✅ **Most stable overall model:** Random Forest  

