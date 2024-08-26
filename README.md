
### README.md
# Hepatitis C Prediction using Logistic Regression

This repository contains code and analysis for a project focused on the Hepatitis C dataset. The main goal is to preprocess the data, conduct exploratory data analysis (EDA), and build a logistic regression model to predict the health status of patients based on various blood test results.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Processing](#data-processing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering](#feature-engineering)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [License](#license)

## Project Overview

This project aims to classify patients as either healthy or suspected of having Hepatitis-related conditions using logistic regression. The dataset includes patient information such as age, sex, and various blood test results.

## Dataset

The dataset used in this project is the Hepatitis C dataset, which can be found on Kaggle. It includes the following columns:

- **Age**
- **Sex**
- **ALB** (Albumin)
- **ALP** (Alkaline phosphatase)
- **ALT** (Alanine transaminase)
- **AST** (Aspartate transaminase)
- **BIL** (Bilirubin)
- **CHE** (Cholinesterase)
- **CHOL** (Cholesterol)
- **CREA** (Creatinine)
- **GGT** (Gamma-glutamyl transferase)
- **PROT** (Total protein)
- **Category** (Target variable: 0 for Healthy, 1 for Suspected)

## Data Processing

- **Handling Missing Values**: Missing values are imputed with the mean of the respective columns.
- **Outlier Removal**: Outliers are removed by using the 1st and 99th percentiles of the data.
- **Feature Scaling**: Features are scaled using the RobustScaler to reduce the impact of outliers.

## Exploratory Data Analysis (EDA)

EDA is conducted to understand the distribution of the data and the relationships between different features. Various plots like box plots, histograms, scatter plots, and heatmaps are used to visualize the data.

## Feature Engineering

Categorical features like `Sex` and `Category` are encoded into numerical values for model training. The following columns are used as features:

- **Age**
- **Sex**
- **ALB**
- **ALP**
- **ALT**
- **AST**
- **BIL**
- **CHE**
- **CHOL**
- **CREA**
- **GGT**
- **PROT**

## Model Training

A logistic regression model is trained using the processed dataset:

- Train-Test Split: The data is split into 80% training and 20% testing.
- Hyperparameter Tuning: GridSearchCV is used to tune hyperparameters such as `penalty`, `C`, and `max_iter`.
- Model Training: The best model is selected and trained on the training data.

## Model Evaluation

The model's performance is evaluated using:

- Accuracy Score: To measure the model's predictive power.
- Confusion Matrix: To analyze the model's classification performance.
- Training vs Testing Accuracy: Visualized using bar plots.

## Dependencies

- Python 3.x
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

## Results

- **Model Accuracy**: The model achieved an accuracy of `XX%` on the test dataset (replace with your actual result).
- **Key Insights**: The EDA provided valuable insights into the distribution of various blood test results and their correlation with the target variable.

