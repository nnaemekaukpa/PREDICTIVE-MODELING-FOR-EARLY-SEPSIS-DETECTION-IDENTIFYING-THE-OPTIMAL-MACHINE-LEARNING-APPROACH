This project involves developing and evaluating machine learning models for predicting sepsis using a time-series medical dataset. The dataset was sourced from [Kaggle's Prediction of Sepsis dataset](https://www.kaggle.com/datasets/salikhussaini49/prediction-of-sepsis/data), which includes various clinical and demographic features. The primary goal is to classify patients as septic or non-septic and explore the factors contributing to sepsis development.

Dataset Information
Source: Kaggle
Features: 44 clinical and demographic variables, including vital signs, lab results, and time-related data (Hour).
Target Variable: SepsisLabel (binary: 1 = septic, 0 = non-septic).
Notable Columns:
Hour: Time of observation.
Patient_ID: Unique identifier for patients.
Clinical features: HR, O2Sat, Temp, MAP, etc.

Key Steps in the Project
Data Preprocessing:

Handling Missing Values: Columns with more than 80% missing data were dropped. Missing values in numeric columns were filled with the median, and categorical columns were filled with the mode.
Feature Engineering:
Combined columns Unit1 and Unit2 into a new feature, Unit.
Dropped irrelevant features: Patient_ID, Hour, and HospAdmTime.
Created a new feature sepsisType to classify sepsis occurrence as:
SepsisBeforeAdm: Sepsis before ICU admission.
SepsisAfterAdm: Sepsis after ICU admission.
NonSepsis: Patients without sepsis.
Exploratory Data Analysis (EDA):

Visualized missing values, age distribution, and class imbalance in SepsisLabel.
Correlation matrix and feature distributions were analyzed to understand relationships between variables.
Model Training and Evaluation:

Algorithms Used:
K-Nearest Neighbors (KNN)
Logistic Regression
Naive Bayes
Decision Tree
Evaluation Metrics:
Accuracy
Confusion Matrix
ROC-AUC Curve
Key Findings:
KNN and Logistic Regression achieved the highest accuracy (98%).
Naive Bayes had the lowest accuracy (92%).
Model Comparison:

A bar chart comparing the accuracy scores of different algorithms was plotted to highlight performance differences.
