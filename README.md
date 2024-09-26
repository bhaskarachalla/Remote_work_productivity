# Remote Work Productivity Analysis

This repository is focused on analyzing and predicting productivity in remote work environments using a dataset that includes various features related to work habits, hours spent, and other factors affecting productivity.

## Table of Contents
- [Overview](#overview)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Outlier Treatment](#outlier-treatment)
- [Models Used](#models-used)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Overview

With the rise of remote work, understanding productivity levels in such environments has become critical. This project seeks to predict productivity based on various factors such as the number of hours worked, tasks completed, and other relevant features. The primary goal is to build models that can predict the productivity levels and help employers or individuals optimize their workflows for better efficiency.

## Data Preprocessing

Before building the models, the dataset underwent several preprocessing steps:
- **Handling Missing Values**: Any missing values were addressed either by filling them with appropriate methods or by removing incomplete records.
- **Feature Standardization**: Features were standardized using techniques like scaling to ensure all variables contribute equally during model training.
- **Categorical Encoding**: Categorical features were encoded using methods like label encoding to ensure they could be used effectively by machine learning models.

### Features

The dataset contains the following key features:
- **Work Hours**: The number of hours an employee works each day.
- **Task Completion**: The number of tasks completed within a certain period.
- **Break Time**: The amount of time spent on breaks.
- **Communication Tools Usage**: Frequency of using communication tools (such as Slack, Email, etc.).
- **Stress Levels**: Self-reported stress levels during remote work.

The target variable is **productivity**, which is a continuous or categorical variable (depending on the approach).

## Feature Engineering

Feature engineering played a significant role in enhancing the predictive power of the models. Some new features were created from existing ones to capture more nuanced patterns in the data, such as:
- **Productivity per Hour**: Calculating productivity based on the ratio of tasks completed to hours worked.
- **Break Efficiency**: Evaluating how effectively break times correlate with productivity.

## Outlier Treatment

Outliers were carefully analyzed to understand their impact on model performance. In some cases, outliers were kept in the dataset to maintain the natural variability and complexity of remote work environments. However, where appropriate, outliers were treated through techniques such as:
- **Capping**: Limiting the maximum value of certain variables.
- **Log Transformation**: Applying log transformation to variables that had skewed distributions due to outliers.

## Models Used

Several machine learning models were implemented to predict productivity levels in a remote work environment. These models include:

1. **Linear Regression**
   - Used for predicting continuous productivity scores. Linear regression provides a simple baseline for comparison.

2. **Random Forest Regressor**
   - A powerful ensemble method that combines multiple decision trees to improve accuracy. The random forest regressor was used for both feature importance analysis and predicting productivity scores.

3. **Neural Network (PyTorch)**
   - A feedforward neural network was constructed to capture complex relationships in the data. This deep learning model is particularly effective at capturing nonlinear patterns and interactions between features.

## Results

The performance of each model was evaluated using metrics such as:
- **R² Score**: Indicates how well the model explains the variance in the productivity scores.
- **Mean Squared Error (MSE)**: Measures the average squared difference between predicted and actual values.
- **Feature Importance**: For models like Random Forest, feature importance scores were analyzed to understand the factors most strongly correlated with productivity.

