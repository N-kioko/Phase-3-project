
### Telecom Customer Churn Analysis

## Table of Contents

- Introduction
- Business Problem
- Objectives
- Data Understanding
- Data Preparation
- Modeling
- Results
- Conclusion
- How to Run
- Dependencies

## Introduction

In the telecommunications industry, customer churn is influenced by several factors, including service quality, customer service effectiveness, and competition. This project employs predictive models like logistic regression and decision trees to anticipate customer churn and help service providers take proactive measures to retain customers.

## Business Problem
Customer retention is crucial for sustaining growth in any telecommunications firm. Customer churn, where a customer stops using a company's services, poses a significant threat. This study aims to analyze the factors contributing to customer churn and predict the likelihood of churn based on customer behavior and characteristics.

## Objectives

- Understand the customer churn rate.
- Identify the most influential factors contributing to customer churn.
- Develop a predictive model to accurately predict customer churn based on past behavior and characteristics.

## Data Understanding

The dataset used in this study is sourced from Kaggle. It contains 3333 observations and 20 variables, including:

#### **State:** Categorical variable indicating the customer's state.
#### **Account length:** Numeric variable indicating the length of the customer account.
#### **Area code:** Numeric variable indicating the area code of the
#### **Phone number:** Categorical variable (likely to be excluded as it won't contribute to churn prediction).
#### **International plan:**  Categorical variable indicating if the customer has an international plan.
#### **Voice mail plan:** Categorical variable indicating if the customer has a voicemail plan.
#### **Number vmail messages:** Numeric variable indicating the number of voicemail messages.
#### **Total day/eve/night/intl minutes:** Numeric variables indicating usage minutes in various time segments.
#### **Total day/eve/night/intl calls:** Numeric variables indicating the number of calls in various time segments.
#### **Total night minutes:** Numeric variables indicating usage minutes in various time segments.
#### **Total day/eve/night/intl charge:** Numeric variables indicating charges in various time segments.
#### **Customer service calls:** Numeric variable indicating the number of customer service calls made by the customer.
#### **Churn:** Binary target variable indicating customer churn (True/False).

#### The variables in the dataset will enable us to explore connection between various customer preferences/behaviours  and churn.

The dataset undergoes several preprocessing steps, including data cleaning, handling missing values, encoding categorical variables, and feature scaling.

## Modeling
Several predictive models are built and evaluated, including logistic regression and decision trees, to identify the most effective model for predicting customer churn.

## Results
The results section presents the evaluation metrics of the models used, such as accuracy, precision, recall, and F1-score. It also discusses the most influential factors identified through the analysis.

## Conclusion
The study concludes with key insights and recommendations for telecommunications firms to reduce customer churn and improve customer retention strategies.

## How to Run

1. Clone the repository.
2. Install the required dependencies.
3. Open the Jupyter Notebook telcom churn.ipynb and run all cells.

## Dependencies
- Python 3.x
- Jupyter Notebook
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn