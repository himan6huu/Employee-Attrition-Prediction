# 📊 Employee Attrition Prediction

An end-to-end Machine Learning project that analyzes employee attrition patterns and predicts whether an employee is likely to leave an organization.

The project combines **Exploratory Data Analysis (EDA), statistical insights, feature analysis, and classification models** to identify the major factors associated with employee turnover.

---

## 🎯 Project Objective

Employee attrition can significantly affect recruitment costs, productivity, and workforce stability.

The objective of this project is to:

- Analyze employee attrition patterns
- Identify factors associated with employee turnover
- Compare multiple classification algorithms
- Evaluate model performance using classification metrics
- Identify important features influencing attrition
- Build a predictive model that can help identify employees at higher risk of leaving

---

## 📌 Key Highlights

- 📊 Exploratory Data Analysis on employee demographics and workplace factors
- 🔎 Attrition analysis across job roles, satisfaction levels, overtime, travel, and job levels
- 🤖 Comparison of Logistic Regression, Random Forest, and Decision Tree models
- 📈 ROC-AUC evaluation
- 🧩 Confusion matrix analysis
- 🔍 Feature importance and coefficient analysis
- ⚖️ Balanced Logistic Regression to address class imbalance
- 📁 Organized visualizations and trained models

---

## 🗂️ Dataset

The project uses the **IBM HR Analytics Employee Attrition dataset**.

The dataset contains employee-level information such as:

- Age
- Monthly Income
- Job Role
- Job Level
- Job Satisfaction
- Environment Satisfaction
- Business Travel
- Distance From Home
- Overtime
- Years at Company
- Years in Current Role
- Years with Current Manager
- Years Since Last Promotion
- Number of Companies Worked
- Marital Status
- Department
- Employee Attrition

## 📁 Project Structure

```text
Employee-Attrition-Prediction/
│
├── data/
│   └── raw/
│       └── WA_Fn-UseC_-HR-Employee-Attrition.csv
│
├── images/
│   └── charts/
│       ├── attrition_by_business_travel.png
│       ├── attrition_by_environment_satisfaction.png
│       ├── attrition_by_job_level.png
│       ├── attrition_by_job_role.png
│       ├── attrition_by_job_satisfaction.png
│       ├── attrition_by_overtime.png
│       ├── attrition_distribution.png
│       ├── balanced_logistic_confusion_matrix.png
│       ├── distance_from_home_vs_attrition.png
│       ├── feature_importance.png
│       ├── final_logistic_confusion_matrix.png
│       ├── model_performance.png
│       ├── monthly_income_vs_attrition.png
│       ├── random_forest_confusion_matrix.png
│       ├── roc_curve.png
│       └── years_at_company_vs_attrition.png
│
├── models/
│   ├── employee_attrition_config.pkl
│   └── employee_attrition_model.pkl
│
├── python/
│   └── notebooks/
│       └── employee_attrition_analysis.ipynb
│
├── powerbi/
├── reports/
├── sql/
├── docs/
├── .gitignore
└── README.md
```


```markdown
## 🔗 Key Files

| Resource | Description |
|---|---|
| [Dataset](data/raw/WA_Fn-UseC_-HR-Employee-Attrition.csv) | IBM HR Employee Attrition dataset |
| [Analysis Notebook](python/notebooks/employee_attrition_analysis.ipynb) | Complete EDA, preprocessing, modeling and evaluation |
| [Trained Model](models/employee_attrition_model.pkl) | Final trained Logistic Regression model |
| [Model Configuration](models/employee_attrition_config.pkl) | Model configuration and preprocessing information |
| [Charts](images/charts/) | Project visualizations and model evaluation charts |

### Target Variable

`Attrition`

| Value | Meaning |
|---|---|
| Yes | Employee left the organization |
| No | Employee stayed |

---
```

---

## 📊 Key Visualizations

### 1. Attrition Distribution

![Attrition Distribution](images/charts/attrition_distribution.png)

### 2. Attrition by Overtime

![Attrition by Overtime](images/charts/attrition_by_overtime.png)

### 3. Attrition by Job Role

![Attrition by Job Role](images/charts/attrition_by_job_role.png)

### 4. Attrition by Job Satisfaction

![Attrition by Job Satisfaction](images/charts/attrition_by_job_satisfaction.png)

### 5. Monthly Income vs Attrition

![Monthly Income vs Attrition](images/charts/monthly_income_vs_attrition.png)

### 6. Feature Importance

![Feature Importance](images/charts/feature_importance.png)

### 7. Model Performance

![Model Performance](images/charts/model_performance.png)

### 8. ROC Curve

![ROC Curve](images/charts/roc_curve.png)

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Data Understanding
     ↓
Data Cleaning & Preprocessing
     ↓
Exploratory Data Analysis
     ↓
Feature Analysis
     ↓
Train-Test Split
     ↓
Model Training
     ↓
Model Evaluation
     ↓
Feature Interpretation
     ↓
Final Attrition Prediction
```
