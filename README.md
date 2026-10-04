# 🎓 Virexo ML Internship — Task 4: Student Performance Analysis & Prediction System

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-v1.2%2B-orange?logo=scikit-learn)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-3776AB?logo=python)](https://seaborn.pydata.org/)
[![Dataset Scale](https://img.shields.io/badge/Dataset-1%2C000%20Rows-green)]()
[![Status](https://img.shields.io/badge/Status-Completed-success)]()

---

## 📌 Executive Summary
This repository houses an end-to-end Machine Learning pipeline developed for the **Virexo ML Internship (Week 4)**. The project evaluates student academic behavioral metrics—including study hours, attendance percentages, previous exam scores, extracurricular involvement, and sleep patterns—to predict student performance outcomes (`Pass` vs. `At Risk`).

Built on an expanded, statistically significant dataset of **1,000 student records**, the solution leverages a **Random Forest Classifier** to capture complex non-linear relationships while maintaining complete model interpretability.

---

## 🛠️ Data Architecture & Cleaning Rigor

To meet top-tier professional standards and ensure scalable model validation, explicit data audits were conducted prior to model training:

| Preprocessing Audit Step | Check Conducted | Audit Result | Status |
| :--- | :--- | :---: | :---: |
| **Missing Values Audit** | `df.isnull().sum()` | **0 Null Values** | ✅ Verified |
| **Duplicate Entries Audit** | `df.duplicated().sum()` | **0 Duplicates** | ✅ Verified |
| **Dataset Scale** | Total Record Count | **1,000 Rows x 7 Columns** | ✅ Verified |
| **Test Set Allocation** | Stratified Split (80/20) | **200 Test Samples** | ✅ Verified |

---

## 📊 Exploratory Data Analysis (EDA)
Comprehensive bivariate EDA was performed using **Seaborn** to isolate primary risk factors:
* **Study Hours Impact:** Boxplot analysis revealed a clear threshold in weekly study hours differentiating passing students from those at academic risk.
* **Attendance vs. Prior Scores:** Scatter plot analysis mapped out feature interactions, confirming that high attendance strongly offsets lower historical scores.

---

## ⚡ Model Performance & Metrics

The **Random Forest Classifier** was trained on 800 samples and evaluated on a robust **200-sample test set**.

### Performance Summary
* **Classification Accuracy:** **89.50%**
* **Train Set Size:** 800 samples
* **Test Set Size:** 200 samples

### Detailed Classification Report

```text
               precision    recall  f1-score   support

  At Risk (0)       0.88      0.87      0.88        87
     Pass (1)       0.90      0.91      0.91       113

     accuracy                           0.90       200
    macro avg       0.89      0.89      0.89       200
 weighted avg       0.89      0.90      0.89       200
