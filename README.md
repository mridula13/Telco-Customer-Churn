# Telco-Customer-Churn

---
 
 ## Objective

 The objective of this project is to build a machine learning model that predicts whether a telecom customer will churn (Yes/No) using the Telco Customer Churn dataset from Kaggle.
 
 ---

 ## Data
 - Source: [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data)
 - Total Samples: 7043 customers
 - Features: 20 input features
 - Target Variable: Churn (Yes / No)

 ---

 ## Data Cleaning
 - The dataset was downloaded using kagglehub and loaded into a Pandas DataFrame.
 - Converted TotalCharges from string to numeric.
 - Replaced missing values in TotalCharges using the median.
 - Dropped customerID since it is only an identifier.
 - Verified that no missing values remained.
 
