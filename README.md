# Google Advanced Data Analytics Capstone

## Project Title
Salifort Motors Employee Retention Predictive Model

## Project Overview
The goal of this project is to conduct Exploratory Data Analysis (EDA) on a recent employee survey provided by Salifort Motor's HR and construct binary classification models such as Logistic Regression, Decision Trees, Random Forests and XGBoost Classifier to classify if an employee is likely to leave or stay the company. The champion model choosen was an XGBoost Classifier with scoring metrics of - 96.6% Accuracy, 90.3% Precision, 89.5% Recall, 0.899 F1-score & 0.974 ROC-AUC. Lastly, the top 4 variables that help in predicting the outcome variable `left` were: `number_project`, `tenure`, `overworked` & `last_evaluation`.

## Table of Contents
- [Business Case](#business-case)
- [Data Overview](#data-overview)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modelling and Evaluation](#modelling-and-evaluation)
- [Conclusion](#conclusion)

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
#### Data Cleaning
- To get a better understanding of the dataset, `df.info()` & `df.describe()` were applied.
- Columns names were standardized in `snake_case`, renamed & spelling corrected as needed.
- Missing values were checked with `df.isna().sum()` and duplicates were removed with `df.drop_duplicates()`
#### Categorical Variables
Before splitting the data for modelling, the variables `department` and `salary` has to be encoded:
- `department` is categorical, so `pd.get_dummies` can be applied.
- `salary` is categorical too, but it's ordinal. Therefore using `cat.codes` would be appropriate.

## Modelling and Evaluation
After modelling with decision trees, random forests & XGBoost classifier, the champion model chosen was the XGBoost classifier as it excelled in all scoring metrics compared to the other 2 models.
![models_score_comparison](https://github.com/justin-97/Google-Advanced-Data-Analytics-Capstone/blob/main/Images/Models%20score%20comparison.png)
The XGBoost classifier comprised of - learning_rate: 0.01, max_depth: None, min_child_weight: 3, n_estimators: 500


## Conclusion

