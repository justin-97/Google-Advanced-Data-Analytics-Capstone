# Google Advanced Data Analytics Capstone

## Project Title
Salifort Motors Employee Retention Predictive Model

## Project Overview
The goal of this project is to conduct Exploratory Data Analysis (EDA) on a recent employee survey provided by Salifort Motor's HR and construct binary classification models such as Logistic Regression, Decision Trees, Random Forests and XGBoost Classifier to classify if an employee is likely to leave or stay the company. The champion model choosen was an XGBoost Classifier with scoring metrics of - 96.6% Accuracy, 90.3% Precision, 89.5% Recall, 0.899 F1-score & 0.974 ROC-AUC. Lastly, the top 4 variables that help in predicting the outcome variable `left` were: `number_project`, `tenure`, `overworked` & `last_evaluation`.

## Table of Contents
- [Business Case](#business-case)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning) 
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Preparation for Modeling](#data-preparation-for-modeling)
- [Modeling: XGBoost Binomial Classification](#modeling-xgboost-binomial-classification)
  - [Model Results on Training Data](#model-results-on-training-data)
  - [XGBoost Predict on Validation Data](#xgboost-predict-on-validation-data)
  - [XGBoost Predict on Test Data](#xgboost-predict-on-test-data)
- [Conclusion and Insights](#conclusion-and-insights)
- [Recommendation and Next Steps](#recommendation-and-next-steps)

## Business Case
Currently there is a high turnover rate among `Salifort Motors`, which is financially costly. HR has provided a recent employee survery & tasked me to analyze the data to come up with ideas for how to increase employee retention.
The goal of this project is to design a machine learning model to predict whether an employee will leave the company based on: `Department`, `No. of projects`, `Average monthly hours`, `Any other data points`.

## Data Overview
- The dataset has 15,000 rows (including headers) & 10 columns.
- The target variable is `left`, while the other variables are features.

![columns_variables](https://github.com/justin-97/Google-Advanced-Data-Analytics-Capstone/blob/3ae8cc3830d8175facb52d15865eeb39163479fb/Images/Salifort%20Motors%20dataset%20variables.png)

## Exploratory Data Analysis(EDA)
After data cleaning, it was discovered that 16.6% of employees left, while 83.4% stayed.
### Data Preparation
Before splitting the data for modelling, the variables `department` and `salary` has to be encoded
- `department` is categorical, so `pd.get_dummies` can be applied
- `salary` is categorical too, but it's ordinal. Therefore using `cat.codes` would be appropriate

## Modelling and Evaluation



