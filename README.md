# Insurance Cost Prediction using Machine Learning 
# Overview
This project applies machine learning techniques to predict individual medical insurance costs based on demographic and health-related features. The goal is to explore how factors such as age, BMI, smoking status, and region impact insurance charges and to evaluate different regression models.

# Dataset
The dataset used in this project contains 1,338 records with the following features:
age: Age of the individual
sex: Gender
bmi: Body Mass Index
children: Number of dependents
smoker: Smoking status
region: Residential region
charges: Medical insurance cost (target variable)

# Data source: Public dataset from GitHub (Machine Learning with R datasets)

# Project Workflow
1. Data Loading & Exploration
Loaded dataset using pandas

Explored structure with .info() and .describe()

Checked distributions and summary statistics

2. Data Preprocessing
Converted categorical variables using one-hot encoding (pd.get_dummies)

Split data into training and testing sets

3. Model Building
Implemented and compared three regression models:

Linear Regression

Ridge Regression

Lasso Regression

4. Model Evaluation
Models were evaluated using:

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

R² Score
# Results
Model	                    MAE	      RMSE	    R² Score
Linear Regression	      4181.19	   5796.28	     0.78
Ridge Regression	      4193.59	   5800.43	     0.78
Lasso Regression	      4182.43	   5797.03	     0.78

# Key Insight
All models performed similarly, with R² ≈ 0.78, indicating good predictive capability.

Regularization (Ridge/Lasso) did not significantly improve performance over standard linear regression.

# Visualizations
Scatter plot of Actual vs Predicted Charges

Regression comparison plots

Boxplot showing higher insurance costs for smokers vs non-smokers

# Key Findings
Smoking status is a major driver of higher insurance costs
BMI and age also significantly influence charges
Regional differences have smaller effects compared to health factor
The relationship between features and charges is not perfectly linear, indicating room for more advanced models

# Limitations
Linear models assume a linear relationship, which may not fully capture real-world patterns
Some important variables (e.g., medical history, income) are missing
Outliers (very high charges) can affect model performance
Interaction effects (e.g., smoker + BMI) are not fully explored
