Project Overview

This project focuses on predicting the physical fitness level of individuals using machine learning techniques. Based on biometric measurements and physical performance test results, individuals are classified as Fit or Unfit.
The project was developed as part of an Introduction to Machine Learning course.

Objectives

Preprocess and analyze biometric and performance data

Engineer meaningful features related to physical fitness

Train and evaluate multiple machine learning models

Compare model performance using standard classification metrics

Identify the most influential features contributing to fitness prediction

Dataset

Name: Body Performance Dataset

Source: Kaggle

URL: https://www.kaggle.com/datasets/kukuroo3/body-performance-data

Samples: ~13,000 individuals

Original Classes: A, B, C, D

Target Variable:

Fit (1): A, B

Unfit (0): C, D

Data Preprocessing

The following preprocessing steps were applied:

Conversion of multi-class labels into binary fitness labels

Label encoding of categorical features (gender)

Removal of missing and invalid values

Feature scaling using StandardScaler

Stratified train-test split (80% train / 20% test)

Feature Engineering

Several engineered features were created to improve model performance:

Body Mass Index (BMI)

Body Fat Ratio

Strength-to-weight ratio

Jump-to-height ratio

Sit-up-to-age ratio

Flexibility-to-height ratio

Final number of input features: 14

Machine Learning Models

The following models were implemented and evaluated:

Logistic Regression

k-Nearest Neighbors (kNN)

Random Forest

XGBoost (Extreme Gradient Boosting)

Hyperparameter tuning was performed using GridSearchCV and RandomizedSearchCV with 5-fold cross-validation.

Evaluation Metrics

Model performance was evaluated using:

Accuracy

Balanced Accuracy

Sensitivity (Recall – Fit)

Specificity (Recall – Unfit)

F1 Score

ROC AUC

Confusion Matrix

ROC curves were generated to visually compare model performance.

Results Summary
Model	Accuracy Sensitivity Specificity ROC AUC
LogReg	79.7%	80.9%	78.3%	0.88
kNN	   79.1%	88.9%	68.0%	0.87
RF	84.1%	88.9%	78.8%	0.92
XGBoost	86.5%	91.6%	80.8%	0.93

XGBoost achieved the best overall performance.

Feature Importance

Random Forest feature importance analysis revealed that:

Flexibility ratio

Strength ratio

Sit-up ratio

Age

Body fat measures

were the most influential predictors of physical fitness.