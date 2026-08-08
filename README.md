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
```
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
## 📊 Exploratory Data Analysis

The exploratory analysis was performed to understand which employee characteristics are associated with higher attrition.

### 🔎 Key Findings

#### 1. Overall Attrition

The dataset contains **1,470 employees**, with approximately **16.1%** classified as having left the organization.

This indicates a significant class imbalance between employees who stayed and employees who left.

---

#### 2. Overtime and Attrition

Employees working overtime show substantially higher attrition compared with employees who do not work overtime.

This suggests that workload and work-life balance may be important areas for employee retention.

---

#### 3. Job Role and Attrition

**Sales Representatives** have the highest observed attrition rate at approximately **39.8%**.

Other roles such as Laboratory Technicians and Human Resources also show relatively higher attrition compared with roles such as Research Director and Manager.

---

#### 4. Monthly Income and Attrition

Employees who left had lower monthly income on average:

- Employees who stayed: **Mean = 6,832.74**
- Employees who left: **Mean = 4,787.09**

The median monthly income was also lower among employees who left.

This suggests that compensation may be associated with employee retention.

---

#### 5. Age and Attrition

Employees who left were generally younger:

- Employees who stayed: **Mean age = 37.56**
- Employees who left: **Mean age = 33.61**

This suggests that younger employees may have a higher tendency to leave.

---

#### 6. Job Satisfaction and Attrition

Attrition was highest among employees with the lowest job satisfaction:

| Job Satisfaction | Attrition Rate |
|---|---:|
| 1 | 22.8% |
| 2 | 16.4% |
| 3 | 16.5% |
| 4 | 11.3% |

The results suggest an association between lower job satisfaction and higher attrition.

---

#### 7. Years at Company and Attrition

Employees who left generally had shorter tenure:

- Employees who stayed: **Mean = 7.37 years**
- Employees who left: **Mean = 5.13 years**
- Median tenure: **6 years vs 3 years**

This highlights the importance of onboarding, engagement, career development, and early employee retention.

---

#### 8. Job Level and Attrition

**Job Level 1** had the highest observed attrition rate at approximately **26.3%**, while Job Level 4 had the lowest at approximately **4.7%**.

This suggests that early-career employees may require additional retention and career-development support.

---

#### 9. Business Travel and Attrition

Employees who travel frequently had the highest attrition rate:

| Business Travel | Attrition Rate |
|---|---:|
| Travel Frequently | 24.9% |
| Travel Rarely | 15.0% |
| Non-Travel | 8.0% |

Frequent business travel may be associated with higher attrition, potentially due to workload or work-life balance considerations.

---

#### 10. Distance From Home and Attrition

Employees who left had a higher average distance from home:

- Employees who stayed: **Mean = 8.92**
- Employees who left: **Mean = 10.63**

The relationship appears weaker than some of the other factors, so distance from home should be considered alongside other employee characteristics.

---

#### 11. Environment Satisfaction and Attrition

Lower environment satisfaction was associated with higher employee attrition.

This suggests that workplace conditions and employee experience may play a role in retention.

---

### 📌 Overall EDA Takeaway

The exploratory analysis indicates that employee attrition is associated with multiple factors rather than a single variable.

Important areas identified include:

- Overtime and workload
- Compensation
- Job satisfaction
- Environment satisfaction
- Job role
- Job level
- Business travel
- Employee age
- Tenure and career progression

These findings were used to guide the subsequent machine learning analysis.
## 🤖 Machine Learning

### Models Evaluated

Three classification algorithms were evaluated:

- Logistic Regression
- Random Forest
- Decision Tree

Because employee attrition is an imbalanced classification problem, model evaluation focused not only on accuracy but also on **Precision, Recall, F1 Score, and ROC-AUC**.

### 📊 Initial Model Comparison

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 89.1% | 68.4% | 33.3% | 44.8% |
| Random Forest | 86.4% | 44.4% | 10.3% | 16.7% |
| Decision Tree | 76.5% | 15.9% | 17.9% | 16.9% |

Although the original Logistic Regression model achieved the highest accuracy, its recall for employees who left was relatively low.

Since identifying potential employee attrition is the primary objective, accuracy alone was not considered sufficient for selecting the final model.

---

## ⚖️ Class Imbalance Handling

The dataset contains significantly more employees who stayed than employees who left.

To improve detection of the minority class, **class-weighted Logistic Regression** was evaluated.

The balanced model increased recall for employees who left from approximately **33.3% to 61.5%**.

This improvement came with a reduction in overall accuracy and precision, demonstrating the trade-off between correctly identifying attrition cases and generating false positive predictions.

---

## 🎯 Threshold Optimization

The default classification threshold of 0.50 was further evaluated using multiple probability thresholds.

The objective was to find a better balance between:

- Precision
- Recall
- F1 Score

The optimized threshold was **0.65**.

At this threshold, the final model achieved:

| Metric | Result |
|---|---:|
| Accuracy | **84.35%** |
| Precision | **43.14%** |
| Recall | **56.41%** |
| F1 Score | **48.89%** |
| ROC-AUC | **75.9%** |
| Decision Threshold | **0.65** |

The optimized model correctly identified **22 of the 39 employees who left** in the test set.

---

## 🏆 Final Model

The final model selected for the project is:

**Class-Weighted Logistic Regression**

with an optimized prediction threshold of **0.65**.

The model was selected because it provides a more useful balance between detecting employees who may leave and limiting false-positive predictions compared with the initial models.

The trained model and configuration are stored in:

```text
models/
├── employee_attrition_model.pkl
└── employee_attrition_config.pkl
