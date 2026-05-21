# Credit Card Fraud Detection

## Project Overview
Machine learning project built in Python and Google Colab to classify credit card transactions as fraudulent or legitimate using the Kaggle Credit Card Fraud Detection dataset.

## Objective
Build and compare classification models for highly imbalanced fraud detection data.

## Dataset
Source:
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Dataset characteristics:
- 284,807 transactions
- 31 numeric features
- Binary target variable ("Class")
- Severe class imbalance (~99.8% non-fraud)

## Tools & Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- ydata-profiling
- Matplotlib
- Seaborn
- Chardet
- Unidecode

## Project Workflow

### 1. Data Upload & Loading
Supports:

- CSV
- Excel
- NPY
- NPZ

Includes:
- automatic encoding detection
- dataframe conversion
- file validation

### 2. Exploratory Data Analysis
Performed:

- dataset inspection
- numeric/categorical detection
- missing value analysis
- imbalance assessment
- profiling report generation

### 3. Preprocessing

Performed:

- train/test split
- stratified sampling
- scaling
- missing value handling
- one-hot encoding detection

### 4. Correlation Analysis

Findings:

- V17: −0.32 correlation with fraud
- V14: −0.30 correlation with fraud

### 5. Model Development

Models tested:

#### k-Nearest Neighbors

Results:

- Excellent majority-class precision
- Fraud recall ≈ 81.6%

#### Decision Tree

Results:

- Fraud classification improved to 84.7%
- Maintained strong majority-class performance

## Key Findings

Decision Tree outperformed kNN on fraud detection while maintaining high precision.

## Repository Structure

```text
credit-card-fraud-detection/
│
├── data/
├── notebooks/
├── images/
├── README.md
└── requirements.txt
