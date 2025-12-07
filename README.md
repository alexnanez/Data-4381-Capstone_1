![](UTA-DataScience-Logo.png)
# Detecting Online Transaction Fraud via Machine Learning

* **This repository holds an attempt at apply machine learning algorithms to detect fraud in an online transaction dataset from the IEEE-CIS Fraud Kaggle challenge (
the Store Sales - Time Series Forecasting Kaggle challenge ([https://www.kaggle.com/competitions/store-sales-time-series-forecasting](https://www.kaggle.com/c/ieee-fraud-detection)).**

## Overview

* The task was to use the features in the transaction and identity datasets to predict if an online transaction is fraudulent.

## Summary of Work

### Data

* CSV Files:
  * sample_submission.csv
  * test_identity.csv
  * test_transaction.csv
  * train_identity.csv
  * train_transaction.csv
* The training dataset has 590,540 instances where the transaction file provides 394 features and the identity file provides 40 for a total of 434 features in the joined data.

### Data Preprocessing

* Checked missing values for each column of both identity and transaction datasets
* Dropped rows with more than 70% values
* Filled missing data with median for numerical features and mode for categorical features

### Exploratory Data Analysis

* Correlation Heatmap
  * Shows correlation between first 20 numerical features of both identity and transaction datasets
* Seaborn Countplot
  * Visualizes distribution of fraud cases
  * Demonstrates class imbalance in data
* Boxplots
  * Top 3 features that are positively correlated with "isFraud" target variable
  * Shows boxplots of these features grouped by "isFraud" (legitimate vs fraudulent)

### Modeling

* Six imbalancing techniques were used before using a Logistic Regression model to fit the data along. A baseline model without any imbalancing technique used was also included. The techniques were:
  1. Random Oversampling
  2. Random Undersampling
  3. SMOTE
  4. SMOTE-ENN
  5. ADASYN
  6. SMOTE-ENN and PCA

### Overview of files in repository

* This repository holds the Jupyter Notebook used for this project and this README file which details the steps of the notebook.

### Software Setup

* The packages that were used for this project are numpy, pandas, matplotlib.pyplot, seaborn, and sklearn.

### Data

* You can download the data at (https://www.kaggle.com/competitions/ieee-fraud-detection/data)
