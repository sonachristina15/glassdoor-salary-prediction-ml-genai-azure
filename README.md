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
- Hypothesis testing
- Feature engineering and selection
- Machine Learning regression
- Model evaluation
- Cross-validation
- Hyperparameter tuning
- Model saving for future deployment

---

## 🎯 Problem Statement

Salary can vary significantly depending on job role, location, company characteristics, industry, sector, and other job-related factors.

The objective of this project is to use Glassdoor job-posting data to:

- Analyze salary patterns across different job attributes
- Identify important factors associated with salary
- Build Machine Learning models to predict salary
- Compare and evaluate model performance
- Understand the business relevance of salary prediction

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

### Initial Dataset Analysis

- **Rows:** 956
- **Columns:** 15
- **Duplicate rows:** 0
- **Null values:** 0

The dataset also contains placeholder values such as `-1`, which were investigated separately during data cleaning.

The `Salary Estimate` column was stored as text and required preprocessing before being used as the target variable for regression.

---

## 🔍 Exploratory Data Analysis

The project performs detailed exploratory analysis to understand the dataset and identify salary-related patterns.

The analysis includes:

### Univariate Analysis

Analysis of individual variables and their distributions.

### Bivariate Analysis

Analysis of relationships between:

- Numerical vs Numerical variables
- Numerical vs Categorical variables
- Categorical vs Categorical variables

### Multivariate Analysis

Analysis of relationships between multiple variables and salary.

The project follows the **UBM approach**:

- **U – Univariate Analysis**
- **B – Bivariate Analysis**
- **M – Multivariate Analysis**

Multiple visualizations were created to identify meaningful patterns and communicate business insights.

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
8. Feature engineering
9. Feature selection
10. Encoding categorical variables
11. Feature scaling where required
12. Preparing the dataset for Machine Learning
13. Splitting the dataset into training and testing sets

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

#### 1. Linear Regression

Linear Regression was used as one of the regression models for predicting salary.

#### 2. Random Forest Regressor

Random Forest Regressor was used as a second regression approach to capture potentially non-linear relationships between the features and salary.

---

## 📈 Model Evaluation

The models were evaluated using three regression metrics:

### Mean Absolute Error (MAE)

MAE measures the average absolute difference between the actual and predicted salary values.

A lower MAE indicates that predictions are closer to the actual values on average.

### Root Mean Squared Error (RMSE)

RMSE measures prediction error while giving greater importance to larger errors.

A lower RMSE indicates fewer or smaller large prediction errors.

### R² Score

R² measures how much of the variation in the target variable is explained by the model.

A higher R² indicates that the model explains more of the variation in salary.

---

## 📊 Model Performance

### Linear Regression

| Metric | Score |
|---|---:|
| MAE | 7.13K |
| RMSE | 14.47K |
| R² | 0.8205 |

### Random Forest Regressor

| Metric | Score |
|---|---:|
| MAE | 12.59K |
| RMSE | 17.92K |
| R² | 0.7248 |

Based on the test-set results, **Linear Regression performed better than the baseline Random Forest model**.

---

## ⚙️ Cross-Validation & Hyperparameter Tuning

GridSearchCV was used to perform hyperparameter optimization for the Random Forest Regressor.

The tuning used **5-fold cross-validation**.

The hyperparameters considered included:

- `n_estimators`
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`

### Best Parameters

```text
n_estimators = 200
max_depth = None
min_samples_split = 2
min_samples_leaf = 1
````

### Tuned Random Forest Performance

| Metric | Baseline Random Forest | Tuned Random Forest |
| ------ | ---------------------: | ------------------: |
| MAE    |                 12.59K |              12.70K |
| RMSE   |                 17.92K |              17.92K |
| R²     |                 0.7248 |              0.7248 |

The tuned Random Forest did **not improve** the test-set performance compared with the baseline Random Forest.

Therefore, based on the models evaluated in this project, **Linear Regression remained the best-performing model**.

---

## 💼 Business Impact

The salary prediction model can potentially support:

* Salary estimation for job seekers
* Salary benchmarking
* Understanding salary patterns across job-related attributes
* Recruiter and employer analysis
* Data-driven compensation insights

However, the predictions should be considered **estimates rather than exact salary values**, because actual compensation can depend on additional factors that are not represented in the dataset.

---

## 💾 Model Saving

The final Linear Regression pipeline was saved using **Joblib** for future deployment and application development.

```text
glassdoor_salary_prediction_model.joblib
```

The saved model was also loaded again successfully as a sanity check.

---

## 🚀 Future Scope

The project can be extended further by:

* Developing an interactive Streamlit application
* Deploying the application to a cloud platform such as Microsoft Azure
* Integrating Generative AI for natural-language explanations of salary predictions
* Improving the model using additional features and larger datasets
* Exploring additional Machine Learning algorithms

---

## 🧰 Technologies Used

| Category                | Technologies                               |
| ----------------------- | ------------------------------------------ |
| Programming Language    | Python                                     |
| Data Manipulation       | Pandas, NumPy                              |
| Data Visualization      | Matplotlib, Seaborn                        |
| Machine Learning        | Scikit-learn                               |
| Regression              | Linear Regression, Random Forest Regressor |
| Model Evaluation        | MAE, RMSE, R²                              |
| Hyperparameter Tuning   | GridSearchCV                               |
| Model Saving            | Joblib                                     |
| Development Environment | Google Colab                               |
| Version Control         | Git, GitHub                                |

---

## 📁 Project Structure

```text
glassdoor-salary-prediction-ml-genai-azure/
│
├── Glassdoor-Salary-Prediction-ML-GenAI-Azure.ipynb
├── glassdoor_jobs.csv
├── glassdoor_salary_prediction_model.joblib
├── requirements.txt
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/glassdoor-salary-prediction-ml-genai-azure.git
```

### 2. Navigate to the project folder

```bash
cd glassdoor-salary-prediction-ml-genai-azure
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

Open:

```text
Glassdoor-Salary-Prediction-ML-GenAI-Azure.ipynb
```

The notebook can be opened using **Google Colab** or **Jupyter Notebook**.

Make sure `glassdoor_jobs.csv` is in the same directory as the notebook.

---

## 📌 Key Takeaway

This project demonstrates an end-to-end Machine Learning workflow for salary prediction using Glassdoor job-posting data.

The workflow includes:

**Data Analysis → Data Preprocessing → EDA → Feature Engineering → Machine Learning → Model Evaluation → Hyperparameter Tuning → Model Saving**

Among the models evaluated, **Linear Regression achieved the strongest test-set performance**, with an R² score of **0.8205** and an MAE of **7.13K**.

The saved model can be used as a foundation for future Streamlit application development, GenAI integration, and cloud deployment using Microsoft Azure.

---

