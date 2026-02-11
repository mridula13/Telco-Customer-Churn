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

 ---

 ## Exploratory Data Analysis (EDA)
 - Around 26% of customers churn, indicating slight class imbalance.
 - Customers with shorter tenure are more likely to churn.
 - Customers with higher monthly charges show higher churn rates.
 - Customers on month-to-month contracts churn significantly more.
 - Customers with lower total charges tend to churn, likely due to shorter tenure.

 Observation: These insights indicate that tenure, contract type, and pricing are strong churn indicators.

 ---

 ## Train-Test Split
 - 80% Training Data
 - 20% Testing Data
 - Stratified to preserve class distribution

 ---

 ## Models Implemented
 ### Base Model: Logistic Regression
 Logistic Regression was chosen as a simple and interpretable baseline model.
 Results:
 - Accuracy: ~0.80
 - ROC-AUC: 0.8416

 ### Improved Model: Random Forest
 Random Forest was used to capture non-linear relationships between features.
 Results:
 - Accuracy: ~0.80
 - ROC-AUC: 0.8433

 ---

 ## Error Analysis
 ### Confusion Matrix
 Both models:
 - Correctly identify most non-churn customers.
 - Struggle slightly more with identifying churners.
 - Produce some false negatives (missed churn customers).

 In churn prediction, minimizing false negatives is important because failing to identify churners leads to lost revenue.

 ### ROC Curve Analysis
 - ROC curves were plotted for both models.
 - Both models perform significantly better than random guessing (AUC > 0.84).
 - Random Forest slightly outperforms Logistic Regression.
 - The performance difference is small.

 ---

 ## Conclusion
 - Both models perform well on the Telco dataset.
 - Random Forest achieved the highest ROC-AUC (0.8433).
 - Logistic Regression performed nearly as well with lower complexity and higher interpretability.

 The performance improvement from Random Forest is negligible, while it adds complexity and computational overhead. Therefore, Logistic Regression is the preferred model due to its simplicity, efficiency, and comparable predictive performance.

