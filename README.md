
==================== Credit Card Fraud Detection ====================
This project uses the credit card dataset found at https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud to train a Machine Learning model to detect credit card transactions that are likely to be fraudulent. This model was built in Google Colab in Python.

The process includes uploading the data into a dataframe; data preparation and preliminary EDA; column renaming; conducting an exploratory data analysis (EDA); preprocessing the data; model implementation; and evaluation of the model's effectiveness. 

Data uploading (lines 1-84) uses a block of code that I developed to be able to support CSV, Excel, NPY, and NPZ files. It will convert them into a dataframe to be used by the rest of the program.

The data preparation and preliminary EDA step (lines 85-149) detects numeric vs categorical columns, displays dataset structure, improves number formatting for readability, and checks for potential text encoding issues.

The column renaming step (lines 150-239) allows the user to rename columns for convenience and readability. If the user chooses to rename a column in the df, the program will display the first 20 distinct non-null values in the column so that the user can clearly see the data that is going to be renamed; then will test the new name to ensure that it's not already in use or using characters that will make processing difficult.

The advanced EDA step (lines 240-339) ensures that the dataframe is loaded; cleans up and normalizes special characters that might interfere with data processing; checks the row count and decides whether to run a minimal profile (for datasets over 50,000 rows) or a full profile (less than 50,000 rows); cleans the filename if necessary; and either renders the profile or allows the user to opt to download it as an HTML file. 

The Interactive Strong Correlation Heatmap with Masking and Clustering step (lines 340-404) creates a correlation heatmap that only displays highly correlated (>.5) or highly inversely correlated (<-.5) factors for use in preliminary analysis.

The # ML-Final-Project
