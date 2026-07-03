# Bengaluru House Price Prediction 🏠📉


## 🚀 Project Overview
Predicting property values in a highly volatile market like Bengaluru requires a robust pipeline capable of handling inconsistent data formatting, structural null values, and complex multi-dimensional scaling. This repository takes raw housing data and processes it through a strict data engineering checklist to feed highly accurate supervised regression models.

---

## 🛠️ Tech Stack & Libraries
- **Language:** Python 3.x
- **Data Engineering:** Pandas, NumPy
- **Machine Learning Architecture:** Scikit-Learn
- **Visualization Ecosystem:** Matplotlib, Seaborn

---

## 📋 Machine Learning Pipeline Workflow

### 1. Exploratory Data Analysis & Diagnostics
- Initial assessment of dataset size (`.shape`) and datatype configuration (`.info()`).
- Identification of structural missing values and high-cardinality features.
- Analysis of class distribution for categorical pillars (`area_type`, `size`, `availability`).

### 2. Rigorous Data Cleansing & Feature Engineering
- **High-Cardinality Dropping:** Dropped the `society` and `availability` variables due to noise and sparse data distribution.
- **Missing Value Imputation:** Replaced missing structural integers for `bath` and `balcony` counts using robust median values.
- **Format Engineering (`total_sqft`):** Built a custom string-splitting parser to convert range elements (e.g., `"1200-1400"`) into their calculated mid-point averages, clearing out non-standard measurements.
- **Label Standardisation:** Normalized terminology variants by converting all instances of "Bedroom" and "RK" into a standard "BHK" label framework.

### 3. Categorical Encoding
- **Ordinal Variable Mapping:** Built an integer-hierarchy mapping system matching sequential keys from `1 BHK` up to extreme variants like `43 BHK`.
- **Label Encoding:** Processed categorical property layouts (`area_type`) into ML-ready values using Scikit-Learn's `LabelEncoder`.

### 4. Statistical Feature Selection
- Generated a Pearson Correlation Heatmap to spot multicollinearity.
- Pruned low-correlation variables (`balcony`, `location`) to isolate the optimal core predictors: **`size`**, **`total_sqft`**, and **`bath`**.

---

## 📊 Evaluation & Model Benchmarking

The cleaned dataset was systematically split into an **80% Training Set** and a **20% Test Set** for validation benchmarking:

| Model Architecture | $R^2$ Score | Mean Absolute Error (MAE) | Root Mean Squared Error (RMSE) |
| :--- | :---: | :---: | :---: |
| Linear Regression (Baseline) | 0.4510 | 53.4201 | 98.1250 |
| Support Vector Regressor (SVR) | 0.2104 | 62.5140 | 117.3102 |
| K-Neighbors Regressor | 0.5912 | 40.1192 | 84.5420 |
| Decision Tree Regressor | 0.5824 | 41.2351 | 85.4410 |
| Random Forest Regressor | 0.6431 | 37.1025 | 79.0211 |
| **Gradient Boosting Regressor (Best Baseline)** | **0.6687** | **35.4120** | **76.1145** |

---

## ⚙️ Hyperparameter Optimization
To maximize generalization, an exhaustive **Grid Search CV (5-fold Cross Validation)** was applied to the top-performing Gradient Boosting Regressor:
