# Telco-Churn-Tree-Based-Classification
Classifying binary label using various tree based algorithms.


# Telco Customer Churn : Project Overview
* Predicted customer's churn rate to prevent and reduce loss of company.
* Applied Cost-sensitive learning as a method for solving imbalanced dataset problems.
* Optimized Tree-based algorithms such as Gradient Boosting Method, Random Forest Classifier and XGBoost (Extreme Gradient Boosting) using GridsearchCV to tuned the best hyperparameters. 
* Evaluated and chose the best model according to ROC-AUC and Recall metric.

## Code and Resources Used 
* **Python Version:** 3.8.5
* **Conda Version:** 4.9.2
* **Packages:** pandas, numpy, matplotlib, seaborn, sklearn, missingpy
* **Dataset:** https://www.kaggle.com/blastchar/telco-customer-churn

## Data Pre-processing

*	Dropped unimportant feature 
* Checked if data was imbalanced
*	Mapped target class label to binary
* Checked features' outlier 
*	Converted feature to numerical
* Imputed missing values using _missingpy_
* Created one-hot encoded features for categorical variables

## Model Training

After made sure every feature has no missing value, the data was split into 80% training set dan 20% test set. Both predictor training and test set contain 30 variables.

I used 3 tree-based algorithms such as **Gradient Boosting Method, Random Forest, XGBoost** and tuned the hyperparameters on each algorithm. The tuned models was evaluated using Recall and ROC-AUC metric to put more focus on false negative part (which customer was predicted as 'stay', but actually 'churn') in order to minimize business loss.

## Model performance

*	**Gradient Boosting Method** : Recall = 51.515 % - ROC-AUC = 85.614 %
*	**Random Forest**            : Recall = 79.857 % - ROC-AUC = 85.510 %
*	**XGBoost**                  : Recall = 77.897 % - ROC-AUC = 85.479 %

The Random Forest model outperformed the other 2 model. 




