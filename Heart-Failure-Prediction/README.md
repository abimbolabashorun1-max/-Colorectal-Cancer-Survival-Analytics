# Heart Failure Prediction Using Machine Learning

## 📌 Executive Summary

This project applies six machine learning models to predict heart failure mortality using clinical records from 299 patients. The goal was to identify the most accurate model for predicting patient outcomes and to determine which clinical features are the strongest predictors of mortality.

**Key Findings:**
- **Best Model:** Tuned Random Forest (Accuracy: 83.33%, AUC-ROC: 0.914)
- **Mortality Rate:** 32.11%
- **Top Predictors:** Time, serum creatinine, ejection fraction
- **Strongest Features:** Ejection fraction and serum creatinine are the most important clinical indicators

---

## 📊 Dataset Overview

**Source:** Heart Failure Clinical Records Dataset  
**Samples:** 299 patient records  
**Features:** 12 clinical features  
**Target Variable:** `DEATH_EVENT` (0 = Alive, 1 = Deceased)

### Feature Descriptions

| Feature | Description |
|---------|-------------|
| **age** | Patient's age in years |
| **anaemia** | Decrease of red blood cells (0 = No, 1 = Yes) |
| **creatinine_phosphokinase** | Level of CPK enzyme in blood (mcg/L) |
| **diabetes** | Whether patient has diabetes (0 = No, 1 = Yes) |
| **ejection_fraction** | Percentage of blood leaving the heart (normal: 50-70%) |
| **high_blood_pressure** | Whether patient has hypertension (0 = No, 1 = Yes) |
| **platelets** | Platelet count in blood (kiloplatelets/mL) |
| **serum_creatinine** | Level of creatinine in blood (mg/dL) |
| **serum_sodium** | Level of sodium in blood (mEq/L) |
| **sex** | Patient gender (0 = Female, 1 = Male) |
| **smoking** | Whether patient smokes (0 = No, 1 = Yes) |
| **time** | Follow-up period in days |

---

## 🔍 Exploratory Data Analysis (EDA)

### Target Distribution

| Outcome | Count | Percentage |
|---------|-------|------------|
| Alive (0) | 203 | 67.89% |
| Deceased (1) | 96 | 32.11% |

**Observation:** The dataset is slightly imbalanced, with more alive patients than deceased. This was addressed by using stratified train-test split.

### Key Visualizations

| Visualization | Key Insight |
|---------------|-------------|
| **Correlation Heatmap** | Weak correlations between features; no multicollinearity issues |
| **Age Boxplot** | Deceased patients tend to be older (median ~70) than alive patients (median ~60) |
| **Ejection Fraction Boxplot** | Deceased patients have significantly lower ejection fraction (median ~25%) compared to alive patients (median ~40%) |
| **Serum Creatinine Boxplot** | Deceased patients have higher serum creatinine levels |
| **Serum Sodium Boxplot** | Deceased patients show slightly lower sodium levels |

---

## 🤖 Machine Learning Models

### Models Implemented

1. **Support Vector Machine (SVM)**
2. **K-Nearest Neighbors (KNN)**
3. **Logistic Regression**
4. **Decision Tree**
5. **Random Forest**
6. **Gradient Boosting**
7. **Tuned Random Forest** (Hyperparameter Optimization)

### Model Performance Comparison

| Model | CV Accuracy | Test Accuracy | AUC-ROC |
|-------|-------------|---------------|---------|
| **Tuned Random Forest** | 87.03% | **83.33%** | **0.914** |
| Random Forest | 84.94% | 83.33% | 0.891 |
| Gradient Boosting | 84.95% | 83.33% | 0.845 |
| Logistic Regression | 83.67% | 81.67% | 0.859 |
| SVM | 80.75% | 76.67% | 0.845 |
| Decision Tree | 77.41% | 73.33% | 0.664 |
| KNN | 76.17% | 70.00% | 0.800 |

**Best Performing Model:** Tuned Random Forest achieved the highest AUC-ROC (0.914), indicating excellent discrimination between alive and deceased patients.

---

## 🏆 Feature Importance Analysis

### Top 5 Most Important Features (Random Forest)

| Rank | Feature | Importance Score |
|------|---------|------------------|
| 1 | **Time** | 0.361 |
| 2 | **Serum Creatinine** | 0.154 |
| 3 | **Ejection Fraction** | 0.129 |
| 4 | **Platelets** | 0.077 |
| 5 | **Age** | 0.077 |

### Top 5 Most Important Features (Gradient Boosting)

| Rank | Feature | Importance Score |
|------|---------|------------------|
| 1 | **Time** | 0.588 |
| 2 | **Serum Creatinine** | 0.122 |
| 3 | **Ejection Fraction** | 0.098 |
| 4 | **Platelets** | 0.068 |
| 5 | **Creatinine Phosphokinase** | 0.056 |

**Insight:** Both models agree that **time** (follow-up period), **serum creatinine**, and **ejection fraction** are the most important predictors of heart failure mortality.

---

## 📈 Key Insights

### Clinical Insights

| Finding | Clinical Implication |
|---------|---------------------|
| **Low Ejection Fraction** | Strong predictor of mortality – patients with low EF should be closely monitored |
| **High Serum Creatinine** | Indicates kidney dysfunction; associated with higher mortality risk |
| **Older Age** | Older patients are at higher risk of mortality |
| **Time Factor** | Longer follow-up periods capture more outcomes; early intervention is critical |

### Model Insights

| Finding | Implication |
|---------|-------------|
| **Random Forest Best** | Ensemble methods outperform single models for this dataset |
| **AUC-ROC 0.914** | Excellent model discrimination – reliable for clinical decision support |
| **Feature Importance** | Ejection fraction and serum creatinine should be prioritized in clinical assessments |

---

## 📁 Repository Structure

## 👤 Author

**Abimbola S. Bashorun**
- GitHub: https://github.com/abimbolabashorun1-max
- Email: bashorun_abimbola@yahoo.com

---

## 📅 Date

June 2026
