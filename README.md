```python
readme_content = """# Bengaluru House Price Prediction 🏠📉

An end-to-end Machine Learning engineering pipeline built to predict real estate property prices in Bengaluru, India. This project covers everything from raw data ingestion and structural diagnostics to custom feature parsing, comparative ensemble benchmarking, and 5-fold hyperparameter optimization.

## 🚀 Project Overview
Predicting property values in a highly volatile market like Bengaluru requires a robust pipeline capable of handling inconsistent data formatting, structural null values, and complex multi-dimensional scaling. This repository takes raw housing data and processes it through a strict data engineering checklist to feed highly accurate supervised regression models.

---

## 🛠️ Tech Stack & Tools
- **Language:** Python 3.x
- **Data Engineering:** Pandas, NumPy
- **Machine Learning Architecture:** Scikit-Learn
- **Visualization Ecosystem:** Matplotlib, Seaborn

---

## 📋 Machine Learning Pipeline Workflow

### 1. Exploratory Data Analysis & Diagnostics
- Initial assessment of dataset dimensionality (`.shape`) and datatype configurations (`.info()`).
- Automated isolation of structural missing values across all dimensions.
- Boundary analysis of highly unique string variables (`society`, `location`).

### 2. Rigorous Data Cleansing & Feature Engineering
- **High-Cardinality Dropping:** Removed the `society` and `availability` variables entirely due to noise and high volumes of missing records.
- **Missing Value Imputation:** Replaced missing structural integers for `bath` and `balcony` counts using robust median values.
- **Format Engineering (`total_sqft`):** Built a custom string-splitting parser to convert range elements (e.g., `"1200-1400"`) into their calculated mid-point averages, clearing out non-standard measurements.
- **Label Standardization:** Normalized layout labels by converting all instances of "Bedroom" and "RK" into a unified "BHK" framework.

### 3. Categorical Encoding
- **Ordinal Variable Mapping:** Created an integer-hierarchy mapping system matching sequential keys from `1 BHK` up to extreme layout variants like `43 BHK`.
- **Label Encoding:** Processed categorical property layouts (`area_type`) into ML-ready values using Scikit-Learn's `LabelEncoder`.

### 4. Statistical Feature Selection
- Evaluated multicollinearity through a Pearson Correlation Heatmap.
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


```

```text
Version 2 of README.md successfully created.

```python
params = {
    'n_estimators': [100, 200, 300],
    'learning_rate': [0.01, 0.05, 0.1],
    'max_depth': [3, 4, 5]
}

```

### Final Optimized Parameters

* `learning_rate`: **0.01**
* `max_depth`: **5**
* `n_estimators`: **200**

### Production Model Results 🏆

* **Final $R^2$ Score:** `0.6924`
* **Final Mean Absolute Error (MAE):** `34.0211`
* **Final Root Mean Squared Error (RMSE):** `73.3412`

---

## 📂 Repository Structure

```bash
├── Bengaluru_House_Data.csv       # Raw Kaggle property dataset
├── Bengaluru_House_Price.ipynb    # Clean Jupyter Notebook containing complete codebase
└── README.md                      # Detailed technical guide and execution summary

```

---

## 💻 How to Run Locally

1. **Clone the Repository:**
```bash
git clone [https://github.com/your-username/bengaluru-house-price-prediction.git](https://github.com/your-username/bengaluru-house-price-prediction.git)
cd bengaluru-house-price-prediction

```


2. **Install Required Environments:**
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

```


3. **Launch Notebook Pipeline:**
```bash
jupyter notebook

```


Open and run all cells in `Bengaluru_House_Price.ipynb` to re-execute data processing, model engineering, and final grid search results.
"""

with open("README-v2.md", "w") as f:
f.write(readme_content)

print("Version 2 of README.md successfully created.")

```
Your Markdown file is ready
[file-tag: code-generated-file-0-1783060878246150618]

Here is the structured markdown document for your GitHub project repository:

```markdown
# Bengaluru House Price Prediction 🏠📉

An end-to-end Machine Learning engineering pipeline built to predict real estate property prices in Bengaluru, India. This project covers everything from raw data ingestion and structural diagnostics to custom feature parsing, comparative ensemble benchmarking, and 5-fold hyperparameter optimization.

## 🚀 Project Overview
Predicting property values in a highly volatile market like Bengaluru requires a robust pipeline capable of handling inconsistent data formatting, structural null values, and complex multi-dimensional scaling. This repository takes raw housing data and processes it through a strict data engineering checklist to feed highly accurate supervised regression models.

---

## 🛠️ Tech Stack & Tools
- **Language:** Python 3.x
- **Data Engineering:** Pandas, NumPy
- **Machine Learning Architecture:** Scikit-Learn
- **Visualization Ecosystem:** Matplotlib, Seaborn

---

## 📋 Machine Learning Pipeline Workflow

### 1. Exploratory Data Analysis & Diagnostics
- Initial assessment of dataset dimensionality (`.shape`) and datatype configurations (`.info()`).
- Automated isolation of structural missing values across all dimensions.
- Boundary analysis of highly unique string variables (`society`, `location`).

### 2. Rigorous Data Cleansing & Feature Engineering
- **High-Cardinality Dropping:** Removed the `society` and `availability` variables entirely due to noise and high volumes of missing records.
- **Missing Value Imputation:** Replaced missing structural integers for `bath` and `balcony` counts using robust median values.
- **Format Engineering (`total_sqft`):** Built a custom string-splitting parser to convert range elements (e.g., `"1200-1400"`) into their calculated mid-point averages, clearing out non-standard measurements.
- **Label Standardization:** Normalized layout labels by converting all instances of "Bedroom" and "RK" into a unified "BHK" framework.

### 3. Categorical Encoding
- **Ordinal Variable Mapping:** Created an integer-hierarchy mapping system matching sequential keys from `1 BHK` up to extreme layout variants like `43 BHK`.
- **Label Encoding:** Processed categorical property layouts (`area_type`) into ML-ready values using Scikit-Learn's `LabelEncoder`.

### 4. Statistical Feature Selection
- Evaluated multicollinearity through a Pearson Correlation Heatmap.
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

```python
params = {
    'n_estimators': [100, 200, 300],
    'learning_rate': [0.01, 0.05, 0.1],
    'max_depth': [3, 4, 5]
}

```

### Final Optimized Parameters

* `learning_rate`: **0.01**
* `max_depth`: **5**
* `n_estimators`: **200**

### Production Model Results 🏆

* **Final $R^2$ Score:** `0.6924`
* **Final Mean Absolute Error (MAE):** `34.0211`
* **Final Root Mean Squared Error (RMSE):** `73.3412`

---

## 📂 Repository Structure

```bash
├── Bengaluru_House_Data.csv       # Raw Kaggle property dataset
├── Bengaluru_House_Price.ipynb    # Clean Jupyter Notebook containing complete codebase
└── README.md                      # Detailed technical guide and execution summary

```

---

## 💻 How to Run Locally

1. **Clone the Repository:**
```bash
git clone [https://github.com/your-username/bengaluru-house-price-prediction.git](https://github.com/your-username/bengaluru-house-price-prediction.git)
cd bengaluru-house-price-prediction

```


2. **Install Required Environments:**
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

```


3. **Launch Notebook Pipeline:**
```bash
jupyter notebook

```


Open and run all cells in `Bengaluru_House_Price.ipynb` to re-execute data processing, model engineering, and final grid search results.

```

```
