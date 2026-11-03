**CUSTOMER CHURN PREDICTION AND ANALYSIS**

Project Overview

This project focuses on analyzing customer churn and developing machine learning models to predict customers who are likely to leave a telecommunications company.

The project combines Data Analytics, SQL, Power BI, Azure Data Factory, and Machine Learning to transform raw customer data into actionable business insights.

The objective is to identify churn patterns, understand key customer behaviors associated with churn, and build predictive models that can support customer retention strategies.

Business Problem

Customer churn directly affects business revenue and long-term customer relationships.

The company wants to understand:

What percentage of customers are churning?
Which customer segments have higher churn rates?
How do contract type, tenure, monthly charges, and services relate to churn?
Can machine learning identify customers who are likely to churn?
What insights can help the business improve customer retention?

Project Objectives

Perform data cleaning and exploratory data analysis.
Analyze churn patterns using SQL.
Build an interactive Power BI dashboard.
Develop a cloud-based data pipeline using Azure Data Factory.
Build and evaluate machine learning models for churn prediction.
Identify important features associated with customer churn.
Provide actionable business recommendations.


Dataset

Dataset: Telco Customer Churn
The dataset contains customer demographic information, subscribed services, account details, billing information, and churn status.

Original dataset dimensions:
Rows: 7,043
Columns: 21


Important Features

Feature-Description

CustomerID-Unique customer identifier

Gender-Customer gender

SeniorCitizen-Whether the customer is a senior citizen

Partner-Whether the customer has a partner

Dependents-Whether the customer has dependents

Tenure-Number of months the customer has stayed

InternetService-Type of internet service

Contract-Contract type

PaymentMethod-Customer payment method

MonthlyCharges-Monthly customer charges

TotalCharges-Total charges accumulated

Churn-Whether the customer left the company
Target variable: Churn
Yes → Customer churned
No → Customer retained


Tools & Technologies

Tool / Purpose

Python / Data cleaning, EDA, and machine learning

Pandas & NumPy / Data manipulation
 
Matplotlib & Seaborn / Data visualization

MySQL / SQL-based analysis

Power BI / Interactive dashboard

Microsoft Azure SQL Database / Cloud data storage

Azure Blob Storage / Dataset storage

Azure Data Factory / ETL pipeline

Scikit-learn / Machine learning

Google Colab / ML development environment

Git & GitHub / Version control and project portfolio

Project Workflow

1. Data Cleaning & Exploratory Data Analysis

Performed data cleaning and exploration using Python.

Tasks included:

Checking missing values and duplicates
Converting TotalCharges into a numerical format
Exploring customer demographics and service usage
Analyzing churn distribution
Identifying patterns in tenure, charges, contracts, and payment methods
Visualizing churn trends

2. SQL Analysis

Used SQL to investigate churn behavior and customer segments.

Analysis included:

Overall churn rate
Churn by contract type
Churn by internet service
Churn by payment method
Churn by tenure groups
Churn by monthly charges
Customer segmentation using CTEs
Multi-dimensional churn analysis
SQL views for reporting

3. Power BI Dashboard

Developed an interactive dashboard to present churn-related insights.

Dashboard components include:

Total customers
Churned customers
Churn rate
Customer retention metrics
Churn by contract type
Churn by tenure
Churn by payment method
Customer and service analysis
Key business insights

4. Azure Data Pipeline

Implemented a cloud-based data pipeline using Microsoft Azure.

Workflow:

Uploaded the cleaned CSV dataset to Azure Blob Storage.
Created Azure SQL Database and destination table.
Configured Azure Data Factory linked services.
Created source and destination datasets.
Mapped columns between source and destination.
Executed the pipeline to load data into Azure SQL Database.
Connected Power BI to Azure SQL Database.

5. Machine Learning

Built machine learning models to predict customer churn.
Data Preprocessing
Removed customer identifier from model features.
Encoded target variable:
No = 0
Yes = 1
Separated training and testing datasets.
Used stratified train-test splitting.
Applied One-Hot Encoding to categorical features.
Applied Standard Scaling to numerical features.
Used Scikit-learn pipelines to prevent preprocessing leakage.

Models Implemented

Logistic Regression-
Used as the baseline classification model.
Provides a simple and interpretable starting point.

Random Forest Classifier-
Used to capture nonlinear relationships.
Applied class balancing to address the imbalance between churn and non-churn customers.

Evaluation Metrics

Models were evaluated using:
Accuracy
Precision
Recall
F1-score
ROC-AUC
Confusion Matrix
Classification Report

Recall and F1-score for the churn class were considered important because identifying customers likely to churn is a key business objective.

Machine Learning Results:

Preliminary Model Results:

The following results were obtained during initial model experimentation. They should be updated with the final results after retraining and final evaluation.

Metric | Logistic Regression | Random Forest

Accuracy | 79.77% | 77.43%
Churn Precision | 65.08% | 56.67%
Churn Recall | 51.34% | 63.64%
Churn F1-score | 0.5740 | 0.5995
ROC-AUC | 0.8425 | 0.8346

Preliminary Observations

Logistic Regression achieved higher overall accuracy.
Random Forest identified a greater proportion of actual churners.
Random Forest achieved a higher churn-class F1-score.
Logistic Regression achieved a higher ROC-AUC score.
Model selection depends on the business trade-off between missed churners and false alarms.

Note: These are preliminary results from model experimentation and may change after final retraining and evaluation.

Feature Importance

Random Forest feature importance was used to identify features that contributed most to predictions.

Top features from the initial model included:

Feature - Importance

Tenure - 0.1115
TotalCharges - 0.1082
MonthlyCharges - 0.0968
Month-to-month Contract - 0.0863
OnlineSecurity = No - 0.0502
Two-year Contract - 0.0435
TechSupport = No - 0.0331
Fiber optic Internet - 0.0329
Electronic check Payment - 0.0322
These results indicate that customer tenure, billing information, contract type, and subscribed services are important predictive features.

Feature importance represents predictive contribution and does not establish causation.

**Key Business Insights**

Initial analysis identified several churn patterns:

Month-to-month customers exhibited substantially higher churn than customers on longer contracts.

Customers with shorter tenure were more likely to churn.

Customers using fiber optic internet showed higher churn rates in this dataset.

Electronic check users had higher churn rates than customers using automatic payment methods.

Customers without online security or technical support showed higher churn rates.

Customers with higher monthly charges tended to exhibit higher churn.

These findings can help the business design targeted customer retention strategies.

**Business Recommendations**

Based on the analysis:

Introduce retention campaigns for month-to-month customers.

Provide incentives for customers to switch to longer-term contracts.

Focus onboarding and engagement efforts on new customers.

Review pricing and service quality for high-churn customer segments.

Promote online security and technical support services.

Encourage automatic payment methods where appropriate.

Use churn prediction scores to prioritize retention outreach.

These recommendations are based on observed patterns and should be validated through business experiments.
