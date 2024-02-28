# ✨ Predicting Credit Card Approvals

## About the project:
Commercial banks receive a lot of applications for credit cards. Many of them get rejected for many reasons, like high loan balances, low income levels, or too many inquiries on an individual's credit report, for example. Manually analyzing these applications is mundane, error-prone, and time-consuming (and time is money!). Luckily, this task can be automated with the power of machine learning and pretty much every commercial bank does so nowadays. In this notebook, we will build an automatic credit card approval predictor using machine learning techniques, just like the real banks do.

## About the dataset:
The dataset contain the most important features of a credit card application. They include <code>Gender</code>, <code>Age</code>, <code>Debt</code>, <code>Married</code>, <code>BankCustomer</code>, <code>EducationLevel</code>, <code>Ethnicity</code>, <code>YearsEmployed</code>, <code>PriorDefault</code>, <code>Employed</code>, <code>CreditScore</code>, <code>DriversLicense</code>, <code>Citizen</code>, <code>ZipCode</code>, <code>Income</code> and finally the <code>ApprovalStatus</code>. 

## Key takeaway: 
Tackled some of the most widely-known preprocessing steps such as scaling, label encoding, and missing value imputation. We finished with a machine learning model to predict if a person's application for a credit card would get approved or not given some information about that person. 

#### **The best model turned out to yield an accuracy score of 85% and the respective best parameters are <code>{'max_iter': 100, 'tol': 0.01}</code>**

In the future, I would like to train models such as Random Forest, KNN, and XGBoost and compare their performances to the Logistic Regression model. The models would be compared based on ROC Curves and AUC. 

## Procedure:
1. Importing the data and the necessary libraries
2. Inspect the data
   - The dataset has a mixture of numerical and non-numerical features. Specifically data that are of float64, int64 and object types.
   - The dataset also contains values from several ranges.
   - The dataset has missing values, which are labeled with '?'.
3. Replaced all '?' with NaNs.
4. Impute the missing values with mean imputation for numeric columns.
5. Impute the missing values with the most frequent values as present in the non-numeric columns.
6. Label encoding to convert the non-numeric data into numeric.
7. Randomly split the data into train and test sets.
8. Normalize the dataset so all the values are within the range of 0-1.
9. Fit a logistic regression model (mainly used for classification tasks like these)
10. Evaluate the model using a confusion matrix
    - The model was able to yield an accuracy score of almost 84%.
11. Can the model be made better?
    - We perform a grid search of the model parameters to improve the model's ability to predict credit card approvals.
    - We will grid search over the following two hyperparameters: tol and max_iter.
    - We will also instruct GridSearchCV() to perform a cross-validation of five folds.
    - The best model described above.
    
## Skills used:
* Python Libraries: Pandas, Numpy, Scikit-Learn
* Statistics: Logistic Regression

#### The project was completed using DataCamp resources.
