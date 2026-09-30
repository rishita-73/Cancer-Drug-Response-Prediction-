# 🧬 Cancer Drug Response Prediction

A machine learning project for predicting **cancer cell line sensitivity to anti-cancer drugs** using the **Genomics of Drug Sensitivity in Cancer (GDSC)** dataset.

## 📌 Project Overview

This project analyzes **240K+ drug–cell line interactions** from the GDSC dataset and uses **LN_IC50** as the primary measure of drug response.

The problem is formulated as a binary classification task to predict whether a cancer cell line is **Sensitive** or **Resistant** to a particular drug.

Three gradient boosting models were implemented and compared:

- XGBoost
- LightGBM
- CatBoost

**LightGBM achieved approximately 95% classification accuracy** in the project's evaluation setup.

## 🎯 Objectives

- Analyze large-scale cancer drug response data
- Understand patterns associated with drug sensitivity
- Clean and preprocess GDSC data
- Transform LN_IC50 into sensitivity classes
- Train and compare multiple ML models
- Evaluate model performance

## 📊 Dataset

The project uses the **GDSC (Genomics of Drug Sensitivity in Cancer)** dataset.

The dataset contains information about:

- Cancer cell lines
- Anti-cancer drugs
- Drug targets and pathways
- Cancer types
- Drug concentration ranges
- LN_IC50
- AUC
- RMSE
- Z-score

### Target Variable — LN_IC50

**LN_IC50** represents the natural logarithm of the IC50 value.

IC50 is the concentration of a drug required to inhibit approximately 50% of cell viability.

- Lower LN_IC50 → Higher drug sensitivity
- Higher LN_IC50 → Lower drug sensitivity / greater resistance

The response was converted into two classes:

```text
Sensitive
Resistant
```

## ⚙️ Methodology

### 1. Data Preprocessing

- Loaded and inspected the GDSC dataset
- Handled missing and inconsistent values
- Removed unnecessary information
- Processed numerical and categorical features
- Prepared the dataset for machine learning

### 2. Exploratory Data Analysis

Analyzed:

- Drug response distributions
- Cancer types
- Drug targets and pathways
- LN_IC50 distribution
- Response-related patterns

### 3. Feature Engineering

Relevant drug, cancer cell line, pathway, and response-related information was transformed into machine-learning-compatible features.

### 4. Model Training

The following classification models were implemented:

| Model | Description |
|---|---|
| XGBoost | Gradient boosting classifier |
| LightGBM | Fast, leaf-wise gradient boosting |
| CatBoost | Gradient boosting with categorical feature handling |

### 5. Prediction Pipeline

```text
GDSC Dataset
      ↓
Data Cleaning
      ↓
Exploratory Data Analysis
      ↓
Feature Engineering
      ↓
Train / Test Split
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Sensitive / Resistant Prediction
```

## 📈 Results

The trained models were evaluated using classification performance metrics.

**LightGBM achieved approximately 95% accuracy** in the project's evaluation setup and showed the strongest performance among the tested models.

> **Note:** The reported accuracy is specific to the project's dataset preparation and evaluation methodology and should not be interpreted as clinical-level predictive performance.

## 🧰 Tech Stack

```text
Python
Pandas
NumPy
Scikit-learn
XGBoost
LightGBM
CatBoost
Matplotlib
Seaborn
Jupyter Notebook
```

## 💡 Applications

This project demonstrates potential applications of machine learning in:

- Cancer drug response prediction
- Precision oncology research
- Drug screening
- Drug-response pattern analysis
- Biomarker research
- Personalized treatment research

## Note
This project was replicated as part of hands-on learning and practice to understand the complete workflow of cancer drug response prediction using machine learning.


