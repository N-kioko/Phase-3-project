
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

## Data Preparation

The Kaggle data Syriatel  Customer Churn dataset from Kaggle had no missing Values. The step involves spliitting dataset into training and testing sets to avoid data leakages.

## Modeling
Several predictive models are built and evaluated, including logistic regression and decision trees, to identify the most effective model for predicting customer churn.
1. The baseline Model; class imbalance in the data is detected in the data due to poor F1 , precision and recall score.  It is necessary to conduct SMOTE(Sythetic Minority Oversampling Technique)
2. The second Model is fitted on the resampled data.  The Model overfits as it has better F1 , Precision and recall score on train data.
3. To deal with the overfitting problem, Model Regularization is used hence fitting Ridge and Lasso Models. The results  do not differ from the the second model.
4. Decision Tree is finaly fitted on  resampled data. The  accuracy on training data is  71% and 91% on testing data. This stand to be the best perming model.

## Results

## -**Performance Metrics of the baseline model performance**

**Precision: Train: 0.568, Test: 0.579**

The precision values for both the train and test sets are similar, which suggests that the model has a consistent rate of correctly identifying positive instances across both sets. However, the precision is relatively low, indicating that a significant number of predicted positives are actually false positives.

**Recall: Train: 0.180 Test: 0.176**

The recall values are quite low for both train and test sets, which means the model is missing a large number of actual positive instances. This might suggest that the model is not very sensitive and is underfitting the positive class.

**Accuracy: Train: 0.866 Test: 0.857**

The accuracy is relatively high, but this might be misleading if the dataset is imbalanced (i.e., there are many more negatives than positives). High accuracy in such cases could simply reflect the model's ability to predict the majority class correctly.

**F1 Score: Train: 0.274 Test: 0.270**

The F1 score, which is the harmonic mean of precision and recall, is quite low for both train and test sets. This indicates a poor balance between precision and recall, reflecting overall weak performance in identifying the positive class.

## -Performance Metrics of  Second Model  After Solving Class Imbalance with  SMOTE

**Precision: Train Precision: 0.709, Test Precision: 0.324**

Precision on the training data is high, but it drops significantly on the test data. This suggests that while the model performs well in identifying positive instances during training, it struggles to maintain this performance on unseen data. This drop in precision could be due to overfitting.

**Recall: Train Recall: 0.749, Test Recall: 0.732**

Recall is relatively consistent between training and testing. This means the model is fairly good at identifying positive instances across both datasets, although it might not capture all possible positive cases.

**Accuracy: Train Accuracy: 0.721, Test Accuracy: 0.731**

Accuracy is fairly similar for both training and testing, which is a good sign.

**F1 Score: Train F1: 0.729, Test F1: 0.450**

The F1 score, which balances precision and recall, is much lower on the test data compared to the training data. This indicates that the model might be performing well on precision and recall during training but is not generalizing well to new data.

In summary, the Evaluation Metrics seem to be performing well on training data but not very well on the test data. This suggests overfitting and need to regularrize the model 


## - **Performance Metrics of  Ridge and Lasso Models**

 The model evaluation Metrics for both lasso and ridge models seem constant the Log_reg model trained asfter conducting SMOTE. We therefore condlude that the second model is the best we have for predicting Churn among the Syria Tel Customers.

 ## - **Performance Metrics of the Decision Tree** 

The Decision Tree model performs well on both the training with an accuracy of 71% and testing data, with a high accuracy score of 91%. This suggests that the model is not overfitting the data and can generalize well to new, unseen data. This makes it the most accurate prediction model for the syriatel data.



## Conclusion
The study concludes with key insights and recommendations for telecommunications firms to reduce customer churn and improve customer retention strategies.

#### **Objective 1 :** Understand the customer churn rate

The SyriaTel customer churn rate is approximately 14%, which means that out of every 100 customers, 14 are expected to leave the company.

#### **Objective 2 :** Estimate the churn  effects  on the company's revenue.

The  14% churn rate is approximately results to  approxinately 15% of revenue loss. This is a significant number and  there is need for  immediate attention to improve customer retention.


#### **Objective 3 :** Develop a predictive model that can accurately predict the likelihood of customers churn based on their past behavior and characteristics.

The second model, which is a Ridge Regression model trained on SMOTE data, has the Consistent performance metrics and is the most accurate for predicting customer churn among the Syria Tel Customers. The model has a precision of 0.709, a recall of 0.749, and a F1 score of 0.729 on the test data. This indicates that the model is capable of identifying customers who are most likely to churn.

The decision Tree model stands out to be one of the most accurate model to predict customers churn. The model has accuracy of 71% on training data and 91% on the test data showing its ability to generelize well on new data.


### **Recomendation**

The results of this analysis show that SyriaTel has a significant customer churn rate of approximately 14%. This is a significant issue, as it results in a loss of approximately 15% of revenue. To address this issue, the following recommendations have been made:

1. 14% client loss with an estimate loss of the company's 15% revenue could be detrimental to the company on both profit mergins, snd sustainability.  There is need to Identify the most influential factors contributing to customer churn from the correlation matrix. There is need for collecting data that is more client_centred so as to explore characteristics of clients who are likely to be lost for remediation purposes.

2. Based on the results, we recommend the use of a Decision Tree model for predicting customer churn. This model has a high accuracy score, making it a reliable choice for this specific problem. The model can be fine-tuned and regularized to improve its performance. Additionally, the collected data should be more client_centred to provide more accurate and relevant insights for identifying the most influential factors contributing to customer churn.

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