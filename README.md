==================== Credit Card Fraud Detection ====================

This project uses the credit card dataset found at https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud to train a Machine Learning model to detect credit card transactions that are likely to be fraudulent. This model was built in Google Colab in Python.

The process includes uploading the data into a dataframe; data preparation and preliminary EDA; column renaming; conducting an exploratory data analysis (EDA); preprocessing the data; model implementation; and evaluation of the model's effectiveness. 

Data uploading (Code block 1) uses a block of code that I developed to be able to support CSV, Excel, NPY, and NPZ files. It will convert them into a dataframe to be used by the rest of the program.

The data preparation and preliminary EDA step (Code Block 2) detects numeric vs categorical columns, displays dataset structure, improves number formatting for readability, and checks for potential text encoding issues.

The advanced EDA step (Code block 3) ensures that the dataframe is loaded; cleans up and normalizes special characters that might interfere with data processing; checks the row count and decides whether to run a minimal profile (for datasets over 50,000 rows) or a full profile (less than 50,000 rows); cleans the filename if necessary; and either renders the profile or allows the user to opt to download it as an HTML file. 

The Preprocessing step (Code block 4) selects the target as per user input; tests for problems in the data; reports on whether there is any missing data (and how much is missing); splits the features and the target; detects the column types; splits training data from testing data (stratifies in case of unbalanced datasets); imputes missing data where necessary; one-hot encodes data where necessary; and scales the data.

The Correlation Analysis step (Code block 5) displays the training data in a full correlation heatmap; shows the top 10 positive and negative features correlated with the target; and displays absolute correlations heatmap with annotations for correlations above 0.3 and below -0.3.
Results: V17 has a correlation of -0.32 with Class, and V14 has a correlation of -0.3 with Class. All other features were less strongly correlated with Class.

The kNN Analysis block (Code block 6) uses binary grouping, uses a stratified sample for training data, uses a range of 3-8 nearest neighbors to optimize speed, and limits to the top correlated features to reduce dimensionality. 
Results: 
