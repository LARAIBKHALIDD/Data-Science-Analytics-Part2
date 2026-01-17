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



# Task 2: Customer Segmentation Using K-Means

## **Task Objective**
The objective of this task is to segment customers based on their spending habits using unsupervised learning. By identifying distinct customer groups, we aim to propose tailored marketing strategies that enhance engagement and sales efficiency.

---

## **Approach**
1. **Dataset:** Mall Customers Dataset (`Mall_Customers.csv`).  
2. **Data Preprocessing:**
   - Cleaned column names to remove spaces and special characters.  
   - Selected relevant features: `Age`, `Annual Income`, and `Spending Score`.  
   - Standardized features using `StandardScaler`.  
3. **Exploratory Data Analysis (EDA):**
   - Plotted distributions of age, income, and spending score.  
   - Created scatter plots to visualize customer behavior by gender.  
4. **Clustering:**
   - Used **K-Means clustering** to segment customers.  
   - Determined optimal number of clusters (k=5) using the **Elbow method**.  
5. **Dimensionality Reduction:**
   - Visualized clusters in 2D using **PCA** and optionally **t-SNE**.  
6. **Marketing Strategy Development:**
   - Analyzed cluster centers to understand customer characteristics.  
   - Assigned tailored marketing strategies for each cluster.

---

## **Results & Findings**
- **Optimal Clusters:** 5 clusters were identified, each representing a distinct customer segment.  
- **Cluster Insights:**
  - **Cluster 0:** Younger customers with low spending → budget-friendly deals.  
  - **Cluster 1:** High-income, high-spending customers → premium offers & loyalty programs.  
  - **Cluster 2:** Low-income, low-spending customers → value bundles & promotions.  
  - **Cluster 3:** Young, high-spending customers → trendy products & social media campaigns.  
  - **Cluster 4:** Older customers with moderate spending → personalized recommendations & seasonal offers.  
- **Visualizations:**
  - PCA and t-SNE plots clearly show well-separated clusters.  
  - Scatter plots reveal spending patterns by age and income.  
- **Business Application:**  
  Using these clusters, marketing teams can **target customers more effectively**, optimizing campaigns based on age, income, and spending behavior.

---

## **Conclusion**
This task demonstrates how **unsupervised learning** can reveal hidden patterns in customer behavior. By combining **K-Means clustering**, **dimensionality reduction**, and **strategy assignment**, businesses can create **data-driven marketing campaigns** tailored to each customer segment.


