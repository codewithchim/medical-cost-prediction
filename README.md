Predicting Medical Costs Using Machine Learning
Project Overview

This project explores the prediction of individual medical insurance costs using demographic and lifestyle data. The objective was to identify key drivers of healthcare expenses and build regression models to estimate medical charges.

This is a supervised machine learning regression task using real-world-style insurance data.

Dataset

The dataset used in this project is included in this repository as:
insurance_charges_data.csv
It contains 1338 records with the following features:

age
sex
bmi
children
smoker
region
medicalCost (target variable)

Data Cleaning & Preprocessing

Checked for missing values (none found)
Removed duplicate records
Standardized numerical features
Applied one-hot encoding to categorical variables
Created interaction features (e.g. BMI × smoker)

Exploratory Data Analysis (EDA)

Key insights from the analysis:

Medical costs show high variance and outliers
Smokers incur significantly higher costs than non-smokers
BMI and age both positively correlate with medical expenses
Smoking amplifies the effect of BMI and age
Regions are evenly distributed across the dataset

Feature Engineering

One-hot encoding for categorical variables
Interaction terms to capture combined effects:

BMI × smoker
Age × smoker
Age × BMI

Correlation Analysis

Top predictors of medical cost:
Smoking status (~0.79 correlation)
Age (~0.30 correlation)
BMI (~0.20 correlation)

Model Building

Models implemented:
Linear Regression (single predictors)
Multiple Linear Regression (top 3 predictors)
Multiple Linear Regression (all features)

Model Performance

Model	R² Score
Smoking only	0.620
Age only	0.089
BMI only	0.039
Top 3 predictors	0.747
All predictors	0.751

Key Insights

Smoking is the strongest predictor of medical costs
Age and BMI also significantly impact costs
A simplified model using top predictors performs nearly as well as the full model
Combining features improves predictive accuracy

Conclusion

This project demonstrates the ability to:
Perform end-to-end data analysis
Extract meaningful insights from real-world data
Build and evaluate machine learning models
Communicate findings effectively

Future Improvements

Implement Random Forest or Gradient Boosting
Apply regularization techniques (Ridge/Lasso)
Handle skewness using log transformation
Deploy as an interactive dashboard (e.g. Streamlit)

Tools & Technologies

Python

Pandas

NumPy

Matplotlib & Seaborn

StatsModels
