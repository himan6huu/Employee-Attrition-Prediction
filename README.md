# 👥 Employee Attrition Prediction

### Predicting Employee Turnover Risk using Python, Machine Learning, and Data Analytics

---

## 📌 Project Overview

Employee attrition is a major challenge for organizations because unexpected employee turnover can increase recruitment costs, reduce productivity, and affect team performance.

This project uses **Exploratory Data Analysis (EDA)** and **Machine Learning** to analyze employee characteristics and identify employees who may be at higher risk of leaving an organization.

The project follows an end-to-end data analytics and machine learning workflow:

- Data Cleaning & Preparation
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Classification Model Development
- Class Imbalance Handling
- Model Evaluation
- Threshold Optimization
- Feature Importance Analysis
- Business Insights & Recommendations

The final model uses **class-weighted Logistic Regression** with an optimized decision threshold to improve the identification of employees at risk of attrition.

---

## 🎯 Business Problem

Employee turnover can be difficult to predict because attrition is influenced by multiple factors such as workload, compensation, job satisfaction, career progression, and work environment.

This project aims to answer questions such as:

- Which factors are associated with employee attrition?
- Which employee groups have higher attrition rates?
- How does overtime affect employee turnover?
- Does job satisfaction influence attrition?
- Are younger or newer employees more likely to leave?
- Can machine learning identify employees at higher risk of attrition?
- How can HR teams use these insights to improve retention strategies?

---
## 📂 Dataset

**Dataset:** IBM HR Analytics Employee Attrition & Performance Dataset

The dataset contains employee-level information covering demographics, job characteristics, compensation, satisfaction, work experience, and other factors related to employee attrition.

### Key Attributes

- Employee demographics
- Job role and job level
- Monthly income
- Overtime
- Business travel
- Job satisfaction
- Environment satisfaction
- Years at company
- Years in current role
- Years with current manager
- Distance from home
- Attrition status

The raw dataset is stored inside:

```text
data/raw/
## ⚙️ Project Workflow

The project follows an end-to-end analytics and machine learning workflow:

1. **Data Collection**
   - Load the IBM HR Analytics Employee Attrition dataset.

2. **Data Understanding**
   - Examine dataset structure, data types, distributions, and target variable.

3. **Data Cleaning & Preparation**
   - Check for missing values and duplicate records.
   - Prepare numerical and categorical variables for analysis.

4. **Exploratory Data Analysis**
   - Analyze attrition patterns across employee demographics, compensation, job characteristics, satisfaction, overtime, travel, and tenure.

5. **Feature Preparation**
   - Encode categorical variables.
   - Separate features and target variable.
   - Split the dataset into training and testing sets.
   - Standardize features for model training.

6. **Model Development**
   - Logistic Regression
   - Random Forest
   - Decision Tree

7. **Model Evaluation**
   - Accuracy
   - Precision
   - Recall
   - F1 Score
   - ROC-AUC
   - Confusion Matrix

8. **Class Imbalance Handling**
   - Apply class weighting to improve detection of employees who leave.

9. **Threshold Optimization**
   - Evaluate different probability thresholds.
   - Select an optimized threshold based on F1 Score.

10. **Feature Importance Analysis**
    - Examine model coefficients to identify influential factors associated with attrition.

11. **Business Insights**
    - Translate analytical findings into actionable HR insights.

12. **Business Recommendations**
    - Suggest strategies focused on employee retention and early intervention.

---
