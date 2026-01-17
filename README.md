# Data-Science-Analytics-Part2

# Task 1: Term Deposit Subscription Prediction

## **Task Objective**
The objective of this task is to predict whether a bank customer will subscribe to a term deposit as a result of a marketing campaign. This involves understanding customer behavior, training classification models, and using Explainable AI (SHAP) to interpret model predictions.

---

## **Approach**
1. **Dataset:** Bank Marketing Dataset (`bank-full.csv`) from the UCI Machine Learning Repository.  
2. **Preprocessing:**
   - Encoded target column (`y`) as numeric (yes → 1, no → 0).  
   - Converted categorical features to numeric using one-hot encoding.  
   - Split the dataset into training and testing sets (80% train, 20% test).  
   - Scaled numeric features for Logistic Regression.  
3. **Modeling:**
   - Trained **Logistic Regression** and **Random Forest Classifier**.  
   - Evaluated models using **Confusion Matrix**, **F1-Score**, and **ROC-AUC**.  
4. **Explainable AI:**
   - Used **SHAP** to explain top features globally and individual predictions.  

---

## **Results & Findings**
- **Model Performance:**

| Model                  | F1-Score (Class 1) | ROC-AUC  |
|------------------------|------------------|----------|
| Logistic Regression     | ~0.60            | ~0.84    |
| Random Forest           | ~0.67            | ~0.89    |

- **Key Insights from SHAP:**
  - Top features influencing subscription: `duration`, `previous`, `poutcome`, `balance`.  
  - Customers with longer call durations and positive previous outcomes are more likely to subscribe.  
  - Higher account balances increase subscription likelihood.  

- **Business Recommendations:**
  1. Prioritize customers with **previous positive outcomes** or multiple prior contacts.  
  2. Focus on **longer calls**, as they increase subscription probability.  
  3. Tailor marketing based on **balance and demographics** to improve campaign efficiency.  
  4. Use SHAP explanations to **justify marketing decisions** to stakeholders.  

---

## **Conclusion**
This task demonstrates the use of **classification models** and **Explainable AI** for predicting customer behavior in banking. The insights can help design **targeted marketing campaigns** and improve overall efficiency.


This task demonstrates the use of **classification models** and **Explainable AI** for predicting customer behavior in banking. The insights can help design **targeted marketing campaigns** and improve overall efficiency.
