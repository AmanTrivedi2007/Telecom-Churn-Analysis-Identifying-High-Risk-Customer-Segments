# 📉 Telecom Customer Churn Analysis: Identifying High-Risk Segments

## 📌 Project Overview
Customer retention is critical for telecom companies. The goal of this project was to analyze customer demographics and financial behaviors to identify the key drivers of **Customer Churn**. 

By comparing a linear model (Logistic Regression) against a rule-based model (Decision Tree), I focused on extracting **interpretable business insights** to help the marketing team target high-risk groups.

## 📂 Dataset
* **Source:** Synthetic dataset generated using NumPy/Pandas (simulating real-world banking/telecom data).
* **Size:** 1,000 Customer Records.
* **Features:** Credit Score, Geography (France, Spain, Germany), Gender, Age, Tenure, Balance, Number of Products, Has Credit Card, Is Active Member, Estimated Salary.
* **Target:** `Exited` (1 = Churn, 0 = Retained).

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib (Boxplots, Heatmaps, Bar Charts)
* **Machine Learning:** Scikit-Learn (Logistic Regression, Decision Tree Classifier, StandardScaler)

## 📊 Key Findings & Business Insights
While the Logistic Regression model provided a stable baseline accuracy, the **Decision Tree** was utilized to uncover the *logic* behind customer decisions.

### 1. The "Age" Factor 👴
* **Insight:** Age is the #1 predictor of churn.
* **Detail:** Customers **over the age of 50** showed a significantly higher probability of leaving compared to younger demographics.

### 2. The "Geography" Factor 🌍
* **Insight:** Location matters.
* **Detail:** Customers in **Germany** were identified as a high-risk segment compared to France and Spain.

### 3. Financial Activity 💳
* **Insight:** Active members were less likely to churn, confirming that engagement strategies are working.

## ⚙️ Project Workflow
1.  **Data Generation:** Created a realistic dataset with complex relationships (non-linear patterns).
2.  **Exploratory Data Analysis (EDA):**
    * Used **Box Plots** to detect outliers in Age and Balance.
    * Analyzed class imbalance (Churn vs. Retained).
3.  **Preprocessing:**
    * Applied **One-Hot Encoding** for categorical variables (`Geography`, `Gender`).
    * Applied **StandardScaler** to normalize numerical features for Logistic Regression.
4.  **Modeling:**
    * **Logistic Regression:** Achieved ~70.5% Accuracy (Baseline).
    * **Decision Tree:** Achieved ~64.0% Accuracy (Used for Feature Importance analysis).
5.  **Evaluation:**
    * Confusion Matrix analysis.
    * Feature Importance extraction.
 ## 📊 Model Performance & Conclusion
I trained three models to predict customer churn:
1.  **Logistic Regression:** 70.5% Accuracy (Winner 🏆)
2.  **Random Forest:** 70.0% Accuracy
3.  **Decision Tree:** 64.0% Accuracy

**Conclusion:**
The **Logistic Regression** model performed best. This suggests that the relationship between customer features (Age, Geography) and Churn is primarily **linear** (additive). 

While the Random Forest is a more powerful algorithm, it added complexity without improving accuracy for this specific dataset. Therefore, **Logistic Regression is the recommended model for deployment** due to its computational efficiency and interpretability.

## 🚀 Future Scope
* **Model Improvement:** Implement**XGBoost** to improve prediction accuracy by reducing the variance of the single Decision Tree.
* **Hyperparameter Tuning:** Use `GridSearchCV` to find the optimal depth for the tree models.

## 📬 Contact
* **Author:** [Aman Trivedi]
* **LinkedIn:** (https://www.linkedin.com/in/aman-trivedi-626bb3376/)
