# 📊 Marketing Campaign Prediction Analysis
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![ML](https://img.shields.io/badge/Machine%20Learning-Logistic%20Regression-green)](https://scikit-learn.org/)

## 🎯 Overview
This project performs an end-to-end data science analysis on customer marketing data. The goal is to predict the success of marketing campaigns by analyzing customer demographics, income levels, and household structures.

The project transitions from raw, uncleaned CSV data to a refined Machine Learning model capable of identifying high-potential leads for future targeting.

## 🛠️ Tech Stack
- **Data Handling:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn` (Logistic Regression, Pipelines, StandardScaler)

## 📈 Pipeline Phases

### 1. Data Cleaning & Preprocessing
The initial dataset was heavily uncleaned, requiring the following steps:
* **Header Repair:** Fixed misaligned CSV headers and removed metadata rows.
* **Currency Formatting:** Converted string-based income (e.g., "$84,835.00") into numeric floats for calculation.
* **Feature Standardization:** Cleaned categorical text in columns like `Education`, `Marital_Status`, and `Kidhome`.

### 2. Feature Engineering
To improve model accuracy, several new features were derived:
* **Total_Dependents:** Combined child and teen counts to see full household size.
* **Age:** Calculated based on the customer's birth year.
* **Income_per_Capita:** A "Disposable Income" proxy dividing total income by household size.

### 3. Predictive Modeling
* **Algorithm:** Logistic Regression.
* **Strategy:** Implemented a `Pipeline` with `StandardScaler` to prevent data leakage and handle feature scaling.
* **Handling Imbalance:** Used `class_weight='balanced'` to ensure the model effectively identifies the minority of successful campaign responders.

## 🏆 Key Results
* **Model Accuracy:** ~69.82%.
* **Lead Generation:** Successfully generated a prioritized list of **75 high-potential leads** (Probability > 0.65) for future campaigns.

## 📂 Repository Structure
* `Marketing Sales Data.ipynb`: Full analysis and model development.
* `campaign_target_list.csv`: The exported list of high-probability leads.
* `requirements.txt`: Necessary libraries to run the notebook.