# Glassdoor Job Salary Prediction using Machine Learning, GenAI & Microsoft Azure

## 📌 Project Overview

This project focuses on analyzing Glassdoor job-posting data to understand salary patterns and develop a Machine Learning regression model for salary prediction.

The project analyzes factors such as job role, company characteristics, location, industry, sector, company size, and other job-related attributes to understand their relationship with salary.

The project covers:

- Exploratory Data Analysis (EDA)
- Data cleaning and preprocessing
- Outlier analysis
- Data visualization
- Correlation analysis
- Feature engineering and selection
- Machine Learning regression
- Model evaluation
- Cross-validation and hyperparameter tuning
- GenAI integration
- Microsoft Azure integration
- Streamlit application concept

---

## 🎯 Problem Statement

Salary can vary significantly depending on job role, location, company characteristics, industry, and other job-related factors.

The objective of this project is to use Glassdoor job-posting data to:

- Analyze salary patterns across different job attributes
- Identify important factors associated with salary
- Build Machine Learning models to predict salary
- Compare and evaluate model performance
- Provide understandable insights related to salary predictions

---

## 📊 Dataset

The dataset contains **956 job postings and 15 columns**.

The major attributes include:

- Job Title
- Salary Estimate
- Job Description
- Rating
- Company Name
- Location
- Headquarters
- Size
- Founded
- Type of Ownership
- Industry
- Sector
- Revenue
- Competitors

During the initial analysis:

- The dataset contains 956 rows and 15 columns.
- No duplicate rows were found.
- No null values were found.
- Some columns contain placeholder values such as `-1`, which were investigated during data cleaning.
- The `Salary Estimate` column is stored as text and requires preprocessing before being used as the target variable.

---

## 🔍 Exploratory Data Analysis

The project performs detailed exploratory analysis to understand the dataset and identify salary-related patterns.

The analysis includes:

### Univariate Analysis
Analysis of individual variables and their distributions.

### Bivariate Analysis
Analysis of relationships between two variables, including:

- Numerical vs Numerical
- Numerical vs Categorical
- Categorical vs Categorical

### Multivariate Analysis
Analysis of relationships between multiple variables and salary.

The project follows the **UBM approach**:

- **U – Univariate Analysis**
- **B – Bivariate Analysis**
- **M – Multivariate Analysis**

Visualizations are used to identify meaningful patterns and communicate business insights.

---

## 🛠️ Data Preprocessing

The preprocessing workflow includes:

1. Loading the Glassdoor dataset
2. Understanding the dataset structure
3. Checking data types
4. Checking duplicate values
5. Checking missing values
6. Investigating placeholder values
7. Processing the salary estimate column
8. Feature preparation
9. Encoding categorical variables
10. Preparing the dataset for Machine Learning

---

## 🤖 Machine Learning

This project is a **Regression** problem where the objective is to predict salary.

The Machine Learning workflow includes:

- Train-test split
- Feature preprocessing
- Regression model development
- Model comparison
- Model evaluation
- Cross-validation
- Hyperparameter tuning
- Final model selection

### Models Used

- Linear Regression
- Random Forest Regressor

---

## 📈 Model Evaluation

The models are evaluated using multiple regression metrics:

### Mean Absolute Error (MAE)

Measures the average absolute difference between actual and predicted values.

### Root Mean Squared Error (RMSE)

Measures prediction error while giving greater importance to larger errors.

### R² Score

Measures how well the model explains the variation in the target variable.

Using multiple evaluation metrics provides a better understanding of model performance.

---

## ✨ GenAI Component

The project also incorporates a **Generative AI component**.

A Gemini-based GenAI component is considered for providing natural-language explanations and insights related to salary predictions.

The purpose is to make the Machine Learning prediction easier for users to understand rather than providing only a numerical salary prediction.

---

## ☁️ Microsoft Azure

Microsoft Azure is included as part of the project's cloud-based Machine Learning and deployment objectives.

The overall project is designed around an end-to-end workflow:

```text
Data
  ↓
Data Preprocessing
  ↓
Exploratory Data Analysis
  ↓
Feature Engineering
  ↓
Machine Learning
  ↓
Model Evaluation
  ↓
GenAI
  ↓
Cloud / Deployment
