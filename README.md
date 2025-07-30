# 💼 Texas Employee Salary Prediction Using Machine Learning

## 📌 Overview
This project uses machine learning to predict the **annual salaries of public employees in Texas**. It utilizes multiple employee attributes including job title, agency, status, gender, ethnicity, and years of service. The analysis helps uncover patterns in public compensation and provides insight into what factors influence salary levels the most.

---

## 📊 Dataset Summary

- **Dataset Source**: Public employee records (Texas)
- **Key Features**:
  - `agency`, `agency_name`, `class_title`, `class_code`
  - `hrly_rate`, `hrs_per_wk`, `monthly`, `annual`, `employ_date`
  - Demographics: `gender`, `ethnicity`
  - Status: `employment type`
  - Target variable: `annual` (salary)

---

## 🧹 Data Preprocessing

- Removed null and duplicate records
- Extracted `years_of_service` from `employ_date`
- One-hot encoded categorical variables (gender, ethnicity, status)
- Feature selection and scaling

---

## 📈 Exploratory Data Analysis (EDA)

Visualizations included:
- Distribution and boxplots of salary
- Salary by gender and ethnicity
- Top-paying agencies
- Salary vs. years of service
- Correlation heatmap

---

## 🤖 Machine Learning Models

The following regression models were trained and evaluated:

| Model                | MAE    | RMSE   | R² Score |
|---------------------|--------|--------|----------|
| Linear Regression    |   ✔️    |   ✔️    |   ✔️      |
| Decision Tree        |   ✔️    |   ✔️    |   ✔️      |
| Random Forest        |   ✔️    |   ✔️    |   ✔️      |
| XGBoost Regressor    |   ✔️    |   ✔️    |   **Best** |
| Support Vector Regressor (SVR) | ✔️ | ✔️ | ✔️ |

> 🏆 **XGBoost Regressor** gave the best performance in terms of MAE, RMSE, and R².

---

## 🔍 Hyperparameter Tuning

- **RandomizedSearchCV** for Random Forest and XGBoost
- **GridSearchCV** for SVR and Decision Tree
- Improved performance by tuning key parameters such as `max_depth`, `n_estimators`, `C`, and `gamma`

---

## 🔥 Feature Importance (XGBoost)

Top features influencing annual salary:

- `years_of_service`
- `class_title`
- `agency_name`
- `employment_status`
- `gender`, `ethnicity`

---

## 📜 Conclusion

- **Years of service**, job role, and agency are key salary predictors.
- XGBoost outperformed other models with high R² and low error values.
- This project demonstrates how ML can support **salary transparency**, **budgeting**, and **HR analytics** in the public sector.

---

## ⚙️ Tech Stack

- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`
- IDE: Jupyter Notebook

---
