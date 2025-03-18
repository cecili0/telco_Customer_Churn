# Telco Customer Churn Analysis and Predictive Modeling

- Dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Analysis and modeling done using Google Colab
## Exploratory Data Analysis
1. Observed dataset contains 7043 rows and 21 columns.
2. Visualizations performed in [Tableau Public](https://public.tableau.com/app/profile/cecilio.angelo.carelo/viz/TelcoCustomerChurnAnalysis_17423351712660/CustomerData) and within Colab Notebook.
3. Explored bivariate and multivariate relations between churn rate and other possible columns to find strongest connections.
4. Explored data distributions to make sense of the client demographics and other trends in data.

## Data Cleaning Preproccessing
- Removed customerID column
- Removed rows with missing 'TotalCharges' values
- Converted 'SeniorCitizen' column from 1/0 to 'Yes'/'No'
- Converted 'TotalCharges' to numeric column
- One hot encoding on catgorical variables

## Train Test Split
1. Standard 80/20 train-testsplit
2. Used SMOTE-ENN to balance dataset, from 73/26 to 55/44 split in no churn vs churn classes. This was done to try and help predictive models performance on churn class.

## Model Training
6 models were used to train on the dataset, and their precision, recall, F1-score and AUC metrics recorded on predictions using test set. 
- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost
- K-Nearest Neighbours
- Support Vector Machine

From these 6, the Random Forest and XGBoost models were chosen for further tuning based on their scores on the testing set. After hyperparameter tuning, the tuned XGBoost model was found to have the highest performance.
