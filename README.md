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

```text ```
models/
├── employee_attrition_model.pkl
└── employee_attrition_config.pkl

## 🔍 Feature Importance

The final Logistic Regression model was analyzed using its learned coefficients to identify the features most strongly associated with employee attrition.

### Top Influential Features

| Feature | Model Coefficient |
|---|---:|
| Years at Company | +0.918 |
| OverTime | +0.843 |
| Years in Current Role | −0.723 |
| Years with Current Manager | −0.537 |
| Marital Status | +0.474 |
| Number of Companies Worked | +0.428 |
| Years Since Last Promotion | +0.405 |
| Job Satisfaction | −0.394 |
| Environment Satisfaction | −0.386 |
| Total Working Years | −0.377 |

Positive coefficients indicate an association with a higher predicted probability of attrition, while negative coefficients indicate an association with a lower predicted probability.

> **Note:** Model coefficients represent statistical associations within the trained model and should not be interpreted as proof of causation. Categorical variables should also be interpreted in the context of their encoding.

---

## 💡 Business Insights

The analysis suggests that employee attrition is influenced by a combination of workload, job satisfaction, career progression, compensation, travel requirements, and employee tenure.

Key areas requiring attention include:

- Employees working overtime
- Employees with lower job satisfaction
- Employees with lower environment satisfaction
- Early-career and lower-level employees
- Employees experiencing limited career progression
- Employees with frequent business travel
- Employees with shorter organizational tenure

---

## 🎯 Business Recommendations

Based on the analysis, organizations could consider the following strategies:

1. **Monitor overtime and workload**
   - Review workload distribution and identify employees consistently working overtime.

2. **Improve employee satisfaction**
   - Conduct regular employee feedback and engagement surveys.

3. **Strengthen career development**
   - Provide clear promotion paths, training opportunities, and internal mobility programs.

4. **Support early-career employees**
   - Introduce mentoring, onboarding, and development programs for newer employees.

5. **Review business travel requirements**
   - Evaluate travel workloads and provide additional support to frequently traveling employees.

6. **Use predictive analytics for early intervention**
   - Use the model as an early-warning tool to identify employees who may require additional engagement or retention support.

7. **Combine predictions with HR expertise**
   - Model predictions should support—not replace—human judgment and employee context.

---

## 🔍 Feature Importance

The final Logistic Regression model was analyzed using its learned coefficients to identify the features most strongly associated with employee attrition.

### Top Influential Features

| Feature | Coefficient |
|---|---:|
| Years at Company | +0.918 |
| OverTime | +0.843 |
| Years in Current Role | −0.723 |
| Years with Current Manager | −0.537 |
| Marital Status | +0.474 |
| Number of Companies Worked | +0.428 |
| Years Since Last Promotion | +0.405 |
| Job Satisfaction | −0.394 |
| Environment Satisfaction | −0.386 |
| Total Working Years | −0.377 |

Positive coefficients indicate an association with a higher predicted probability of attrition, while negative coefficients indicate an association with a lower predicted probability.

> **Note:** These coefficients represent model associations, not causal relationships.

---

## 💡 Business Insights

The analysis indicates that employee attrition is associated with multiple factors, including:

- Overtime and workload
- Job satisfaction
- Environment satisfaction
- Career progression
- Employee tenure
- Job level
- Business travel
- Compensation
- Job role

The findings suggest that employee retention should be approached using a combination of workload management, career development, employee engagement, and workplace improvements.

---

## 🎯 Business Recommendations

### 1. Monitor Overtime and Workload
Identify employees who consistently work overtime and review workload distribution to reduce excessive work pressure.

### 2. Improve Employee Satisfaction
Use regular employee feedback and engagement surveys to identify workplace concerns early.

### 3. Strengthen Career Development
Provide clear promotion paths, training opportunities, mentoring, and internal mobility programs.

### 4. Support Early-Career Employees
Focus retention programs on newer and lower-level employees through structured onboarding and career development.

### 5. Review Business Travel
Evaluate travel requirements for frequently traveling employees and provide appropriate workload and work-life balance support.

### 6. Use Predictive Analytics for Early Intervention
Use the model as an early-warning tool to identify employees who may require additional engagement or retention support.

### 7. Combine ML Predictions with HR Expertise
Predictions should support HR decision-making rather than replace human judgment or employee-specific context.

---
## 📊 Key Visualizations

### Employee Attrition Distribution

The dataset contains 1,470 employees:

- **1,233 employees (83.9%)** stayed
- **237 employees (16.1%)** left

This class imbalance was considered during model development and evaluation.

### Attrition by Overtime

Employees working overtime showed a substantially higher attrition rate than employees who did not work overtime, highlighting workload and work-life balance as important areas for HR attention.

### Attrition by Job Role

Sales Representatives recorded the highest attrition rate at approximately **39.8%**, followed by Laboratory Technicians (**23.9%**) and Human Resources (**23.1%**).

### Attrition by Job Satisfaction

Employees with the lowest job satisfaction level recorded the highest attrition rate:

- Satisfaction 1: **22.8%**
- Satisfaction 2: **16.4%**
- Satisfaction 3: **16.5%**
- Satisfaction 4: **11.3%**

### Model Performance

The final Logistic Regression model achieved:

- **84.35% Accuracy**
- **43.14% Precision**
- **56.41% Recall**
- **48.89% F1 Score**
- **75.9% ROC-AUC**

The optimized threshold of **0.65** provided a better balance between identifying employees likely to leave and limiting false-positive predictions.

---

## 🏁 Conclusion

This project demonstrates an end-to-end approach to employee attrition analysis using **Python, exploratory data analysis, and machine learning**.

The analysis identified several important areas associated with employee turnover, including overtime, job satisfaction, career progression, tenure, business travel, compensation, and job characteristics.

Multiple classification algorithms were evaluated, with **class-weighted Logistic Regression** selected as the final model after considering the imbalance between employees who stayed and those who left.

Threshold optimization further improved the model's ability to identify potential attrition cases, achieving a **56.41% recall** and **48.89% F1 score** at a threshold of **0.65**.

The project demonstrates how data-driven analysis can help HR teams identify potential retention risks and support more targeted employee engagement strategies.

---

## 🚀 Future Improvements

- Build an interactive **Power BI HR Attrition Dashboard**
- Develop a web-based employee attrition prediction application
- Experiment with advanced ensemble models
- Perform hyperparameter optimization
- Apply explainable AI techniques such as SHAP
- Evaluate the model on additional HR datasets
- Implement continuous model monitoring and retraining

---

## 📌 Project Outcome

**End-to-end Employee Attrition Analytics & Prediction**

**Data → EDA → Feature Engineering → ML Models → Class Balancing → Threshold Optimization → Feature Analysis → Business Insights**

---
## 🤖 Machine Learning & Model Performance

The project uses supervised machine learning to predict whether an employee is likely to leave the organization.

### 🎯 Target Variable

The `Attrition` variable was converted into binary form:

- `0` → Stayed
- `1` → Left

The dataset contains **1,470 employees**, with **237 employees who left** and **1,233 employees who stayed**.

### 🧠 Models Evaluated

Three classification algorithms were compared:

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 89.12% | 68.42% | 33.33% | 44.83% |
| Random Forest | 86.39% | 44.44% | 10.26% | 16.67% |
| Decision Tree | 76.55% | 15.91% | 17.95% | 16.87% |

Initial evaluation showed that **Logistic Regression** provided the strongest overall performance.

### ⚖️ Handling Class Imbalance

Since employee attrition is an imbalanced classification problem, additional evaluation was performed using class-balanced Logistic Regression.

The model achieved:

- Accuracy: **71.68%**
- Precision: **26.09%**
- Recall: **61.54%**
- F1 Score: **36.64%**
- ROC-AUC: **0.759**

The improved recall demonstrates that balancing the classes helped the model identify more employees at risk of leaving.

### 🎚️ Threshold Optimization

Instead of relying on the default classification threshold of `0.50`, multiple probability thresholds were evaluated.

The optimal threshold was identified as:

**0.65**

At this threshold:

- Accuracy: **84.35%**
- Precision: **43.14%**
- Recall: **56.41%**
- F1 Score: **48.89%**

This threshold provided a better balance between identifying potential leavers and limiting false positives.

### 📈 Final Model

**Final Model: Logistic Regression**

**Classification Threshold: 0.65**

The final model achieved an **F1 Score of 48.89%** and **Recall of 56.41%** for employees who left, making it more suitable for identifying potential attrition risks than relying solely on overall accuracy.

### 🔍 Model Interpretability

Feature coefficients were analyzed to understand the factors associated with employee attrition.

The strongest factors included:

- Years at Company
- Overtime
- Years in Current Role
- Years with Current Manager
- Marital Status
- Number of Companies Worked
- Years Since Last Promotion
- Job Satisfaction
- Environment Satisfaction
- Total Working Years
- Job Involvement
- Monthly Income
- Department
- Distance From Home
- Job Level

This makes the model not only predictive but also useful for understanding potential drivers of employee turnover.

## 📊 Visualizations & Key Insights

### 1. Employee Attrition Distribution

The dataset contains **1,470 employees**, of which:

- **1,233 (83.9%)** stayed with the company.
- **237 (16.1%)** left the company.

This highlights a significant class imbalance, which was considered during model development.

---

### 2. Attrition Rate by Overtime

Employees working overtime show a substantially higher attrition rate:

- **OverTime = Yes:** 30.5%
- **OverTime = No:** 10.4%

This indicates that excessive workload and overtime may be important contributors to employee attrition.

---

### 3. Attrition Rate by Job Role

The highest attrition rate was observed among:

- **Sales Representatives:** 39.8%
- **Laboratory Technicians:** 23.9%
- **Human Resources:** 23.1%

Sales Representatives show particularly high attrition compared with other job roles.

---

### 4. Attrition Rate by Job Satisfaction

Employees with lower job satisfaction have higher attrition:

| Job Satisfaction | Attrition Rate |
|---|---:|
| 1 | 22.8% |
| 2 | 16.4% |
| 3 | 16.5% |
| 4 | 11.3% |

The results suggest that improving employee satisfaction may help reduce turnover.

---

### 5. Attrition Rate by Environment Satisfaction

Employees with the lowest environment satisfaction experienced the highest attrition:

- Satisfaction Level 1: **25.4%**
- Satisfaction Level 2: **15.0%**
- Satisfaction Level 3: **13.7%**
- Satisfaction Level 4: **13.5%**

---

### 6. Attrition Rate by Business Travel

Employees who travel frequently have substantially higher attrition:

- **Travel Frequently:** 24.9%
- **Travel Rarely:** 15.0%
- **Non-Travel:** 8.0%

Frequent business travel appears to be an important factor associated with employee turnover.

---

### 7. Attrition Rate by Job Level

The highest attrition occurs at lower job levels:

- **Job Level 1:** 26.3%
- **Job Level 2:** 9.7%
- **Job Level 3:** 14.7%
- **Job Level 4:** 4.7%
- **Job Level 5:** 7.2%

This suggests that early-career and lower-level employees may require greater retention support.

---

### 8. Monthly Income and Attrition

The boxplot shows that employees who left generally had a lower monthly income distribution compared with employees who stayed.

This indicates that compensation may be associated with employee retention, although income alone should not be interpreted as a direct cause of attrition.

---

### 9. Distance From Home

Employees who left tend to show a higher median distance from home compared with employees who stayed.

Longer commuting distances may therefore contribute to employee turnover.

---

### 10. Years at Company

Employees who left generally have fewer years at the company than employees who stayed.

This suggests that employees may be more vulnerable to attrition during the earlier stages of their employment.

---

## 🤖 Model Performance

Three classification models were evaluated:

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 89.12% | 68.42% | 33.33% | 44.83% |
| Random Forest | 86.39% | 44.44% | 10.26% | 16.67% |
| Decision Tree | 76.53% | 15.90% | 17.95% | 16.87% |

Logistic Regression provided the strongest overall performance among the initial models.

Because employee attrition is an imbalanced classification problem, additional evaluation focused on improving the detection of employees who are likely to leave.

---

## ⚖️ Balanced Logistic Regression

A balanced Logistic Regression model was evaluated to give greater importance to the minority **Left** class.

The balanced model achieved:

- Accuracy: **71.77%**
- Precision: **26.09%**
- Recall: **61.54%**
- F1 Score: **36.64%**
- ROC-AUC: **0.759**

The major improvement was in **recall for employees who left**, increasing from approximately **33% to 62%**.

This demonstrates the trade-off between overall accuracy and the ability to identify potential employee attrition.

---

## 🎯 Threshold Optimization

The classification threshold was optimized to improve the balance between precision and recall.

The selected threshold was:

**0.65**

Final performance:

- Accuracy: **84.35%**
- Precision: **43.13%**
- Recall: **56.41%**
- F1 Score: **48.89%**

At this threshold, the model provides a better balance between correctly identifying employees likely to leave and maintaining overall predictive performance.

---

## 📈 ROC-AUC

The Random Forest model achieved a ROC-AUC of approximately:

**0.706**

The Logistic Regression model achieved a ROC-AUC of approximately:

**0.759**

The Logistic Regression model therefore demonstrated stronger discrimination between employees who stayed and employees who left.

---

## 🔍 Feature Importance

The Logistic Regression coefficients identified several important factors associated with employee attrition.

### Strong positive contributors

- **YearsAtCompany**
- **OverTime**
- **MaritalStatus**
- **NumCompaniesWorked**
- **YearsSinceLastPromotion**
- **Department**
- **DistanceFromHome**

### Strong negative contributors

- **YearsInCurrentRole**
- **YearsWithCurrManager**
- **JobSatisfaction**
- **EnvironmentSatisfaction**
- **TotalWorkingYears**
- **JobInvolvement**
- **MonthlyIncome**
- **JobLevel**

The coefficients represent model associations and should not be interpreted as proof of direct causation.

---

## 💡 Business Insights

The analysis highlights several areas that organizations could investigate to reduce employee attrition:

1. **Reduce excessive overtime** and monitor employee workload.
2. **Improve job satisfaction**, particularly among dissatisfied employees.
3. **Pay greater attention to lower job levels**, where attrition is substantially higher.
4. **Review high-risk job roles**, particularly Sales Representatives.
5. **Support employees with long commutes** or greater distance from the workplace.
6. **Monitor employees with frequent business travel**.
7. **Strengthen early-career retention strategies** for employees with fewer years at the company.
8. **Use predictive analytics** to identify employees who may require proactive retention support.

---

## ⚠️ Limitations

- The dataset is imbalanced, with substantially more employees staying than leaving.
- Model performance depends on the available features and historical dataset.
- Correlation and model coefficients do not establish causation.
- The dataset represents a specific organizational context and may not generalize to every company.
- Predictive models should support HR decision-making rather than replace human judgment.

---

## 🚀 Future Improvements

Future versions of the project could include:

- Hyperparameter tuning using GridSearchCV or RandomizedSearchCV.
- Advanced ensemble models such as XGBoost or Gradient Boosting.
- Cross-validation for more robust model evaluation.
- Advanced class-imbalance techniques such as SMOTE.
- Model explainability using SHAP.
- Interactive Power BI dashboards.
- Deployment as a web application using Flask or Streamlit.
- Automated employee attrition risk scoring.
- Integration with real-time HR analytics data.

---

## 🏁 Conclusion

This project developed an end-to-end **Employee Attrition Prediction System** using exploratory data analysis, machine learning, model evaluation, threshold optimization, and feature analysis.

The analysis identified **OverTime, job role, job satisfaction, environment satisfaction, business travel, job level, distance from home, and employment duration** as important factors associated with employee attrition.

Among the evaluated approaches, **Logistic Regression** provided the strongest overall results. After balancing and threshold optimization, the final model achieved an **F1 Score of 48.89%** and **recall of 56.41%** for the attrition class.

The project demonstrates how machine learning can be applied to HR analytics to identify potential attrition risks and provide data-driven insights that can support employee retention strategies.
