# FINANCE DATA AND DATA GENERATION USING SMOTE

This repository contains the code and analysis for a dataset used to predict a binary target variable (`bad_flag`). The dataset includes various features related to account transactions and attributes. Below is a detailed analysis of the dataset and the steps taken to build and evaluate predictive models.

## Dataset Overview

- **Number of Rows:** 96,806
- **Number of Columns:** 1,216
- **Target Variable:** `bad_flag` (binary: 0 or 1)
- **Features:** The dataset contains a mix of numerical and categorical features, including transaction attributes, onus attributes, and bureau enquiry attributes.

### Key Columns:
- `account_number`: Unique identifier for each account.
- `bad_flag`: Binary target variable indicating whether the account is flagged as bad (1) or not (0).
- `onus_attribute_1` to `onus_attribute_48`: Various attributes related to the account.
- `transaction_attribute_1` to `transaction_attribute_7`: Attributes related to transactions.
- `bureau_enquiry_47` to `bureau_enquiry_50`: Attributes related to bureau enquiries.

## Data Preprocessing

### Handling Missing Values
- The dataset contains a significant number of missing values across many columns.
- Missing values were imputed using the mean strategy with `SimpleImputer`.

### Feature Scaling
- Numerical features were scaled using `StandardScaler` to standardize the data for model training.

### Train-Test Split
- The dataset was split into training and testing sets with an 80-20 split.

### Handling Class Imbalance
- The target variable `bad_flag` is highly imbalanced, with a majority of the samples belonging to class 0.
- To address this, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to the training data to balance the classes.

## Model Training and Evaluation

### Logistic Regression
- **Accuracy:** 78.89%
- **Classification Report:**
