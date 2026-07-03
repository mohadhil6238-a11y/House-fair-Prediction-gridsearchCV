# 🏡 Bengaluru House Price Prediction

A Machine Learning project that predicts house prices in Bengaluru using various regression algorithms. The project includes data preprocessing, feature engineering, model training, hyperparameter tuning using GridSearchCV, and price prediction.

## 📌 Project Overview

The goal of this project is to build a machine learning model capable of predicting the price of a house in Bengaluru based on its features such as location, total square feet, number of bedrooms (BHK), bathrooms, and other relevant attributes.

The project follows a complete machine learning workflow:

- Data Understanding
- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis (EDA)
- Model Building
- Hyperparameter Tuning
- Model Evaluation
- House Price Prediction

---

## 📂 Dataset

**Dataset:** Bengaluru House Price Dataset

The dataset contains information such as:

- Area Type
- Availability
- Location
- Size (BHK)
- Total Square Feet
- Bathrooms
- Balcony
- Price

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- GridSearchCV
- Google Colab / Jupyter Notebook

---

## 📊 Machine Learning Workflow

### 1. Data Understanding

- Load the dataset
- Inspect data types
- Check missing values
- Understand feature distributions

### 2. Data Cleaning

- Remove unnecessary columns
- Handle missing values
- Convert data types
- Remove inconsistent entries

### 3. Feature Engineering

- Extract BHK from Size column
- Convert Total Sqft into numeric values
- Encode categorical variables
- Create useful features

### 4. Outlier Detection

- Remove abnormal house prices
- Remove unrealistic square footage values
- Filter location-wise outliers

### 5. Model Building

Regression algorithms used include:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

### 6. Hyperparameter Tuning

GridSearchCV is used to identify the best-performing model and optimize its parameters.

### 7. Model Evaluation

Models are evaluated using:

- Train/Test Split
- Cross Validation
- R² Score
- Mean Squared Error (MSE)

---

## 📁 Project Structure
