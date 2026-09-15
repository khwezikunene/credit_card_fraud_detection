# Credit Card Fraud Detection

## Overview

This project develops and evaluates various machine learning models for detecting fraudulent credit card transactions.

Credit card fraud detection is a highly imbalanced binary classification problem because fraudulent transactions represent only a very small proportion of all transactions. This project investigates how different machine learning approaches can identify fraudulent transactions while controlling the number of legitimate transactions incorrectly flagged as fraud. The project focuses on model performance, class imbalance, threshold selection, and model explainability rather than accuracy alone.

---

## Dataset

The project uses the Credit Card Fraud Detection dataset. The dataset contains anonymised credit card transactions, with a binary target indicating whether each transaction is fraudulent.

The main variables include:

* `Time` - elapsed time between transactions
* `V1` to `V28` - anonymised numerical features
* `Amount` - transaction amount
* `Class` - target variable

The target variable is defined as:

```text
0 = legitimate transaction
1 = fraudulent transaction
```

The dataset is highly imbalanced, making fraud detection substantially more difficult than ordinary binary classification.

## Project Structure

```text
credit-card-fraud-detection/
│
├── data/
│   ├── raw/
│   │   └── creditcard.csv
│   └── processed/
│
├── notebooks/
│   └── 01_data_exploration.ipynb
│
├── src/
│   ├── __init__.py
│   ├── data_preprocessing.py
│   ├── train.py
│   ├── evaluate.py
│   └── predict.py
│
├── models/
│
├── reports/
│   └── figures/
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

---

## Methodology

The project will follow an end-to-end machine learning workflow:

```text
Raw transaction data
        ↓
Exploratory data analysis
        ↓
Data preprocessing
        ↓
Train/test split
        ↓
Class imbalance handling
        ↓
Model training
        ↓
Model evaluation
        ↓
Threshold optimisation
        ↓
Model explainability
        ↓
Final model
```

The following classification approaches will be investigated, including:

* Logistic Regression
* Random Forest
* Gradient Boosting / XGBoost
* Imbalance-aware approaches such as class weighting and SMOTE

--

## Explainability

Model explainability will be investigated using feature importance and SHAP-based analysis. The aim is to identify which transaction characteristics contribute most strongly to model predictions and to examine individual fraud predictions.
