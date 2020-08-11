# Telecom Customer Churn Classification: Project Overview
* I created this tool to predict whether telecome customer will churn or not (Accuracy = 81.26%, 'need more data to increase accuracy'). We use phone everyday in our daily life, make calls to connect with people. Some time people change their network because of many reasons so i did this project to check what is main reason customers churn from network and created a model which will predict churning of clients.
* Get dataset from Kaggle datasets [Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)
* Perform exploratory data analysis.
* Perform feature engineering.
* Built model and optimize it.
## Code and Resources Used
**Python Version:** 3.7 <br>
**Packages:** numpy, pandas, matplotlib, seaborn, plotly, sklearn, lightgbm, xgboost, pickle.
## Exploratory Data Analysis
In EDA i looked for churn customers ratio, gender ratio in churn customers, churn rate aged and non aged customers, duration of customers with company, monthly customers, payments, difference in customers charges, customers with active services and their effects on customer billing.<br>
**Visualization:**<br>
![deleted or not found](https://github.com/zeeshan-akram/Telecom-Customer-Churn-Classification/blob/master/duration-cust-with-company.png)
![deleted or not found](https://github.com/zeeshan-akram/Telecom-Customer-Churn-Classification/blob/master/internet-monthly-charges.png)
![deleted or not found](https://github.com/zeeshan-akram/Telecom-Customer-Churn-Classification/blob/master/churn-ratio.png)
![deleted or not found](https://github.com/zeeshan-akram/Telecom-Customer-Churn-Classification/blob/master/churn-cust-gender.png)
![deleted or not found](https://github.com/zeeshan-akram/Telecom-Customer-Churn-Classification/blob/master/monthly-customers.png)
![deleted or not found](https://github.com/zeeshan-akram/Telecom-Customer-Churn-Classification/blob/master/no-customers-active-services.png)
## Feature Engineering
After EDA I perform feature engineering to get relative data for modeling. I also hypertune models to get best parameters of models<br> 
**Performed following operations:**
* Check Pearson correlation.
  * Removed correlated predictors to reduce multicolinearity.
  * Removed features with very low correlation with target variable.
* Perform encoding operation to categorical data.
## Model Building
I tried different classification models to get know which one perform well.
**Models I tried for modeling:**
* Decision Tree
  It is modeling approach used in statistics, data mining and machine learning.
* Boosting Techniques
  They improve the prediction power by training a sequence of weak models or week learners.
* Random Forest
  Ensemble learning method for classification, regression. Handle missing values and maintain the accuracy of a large proportion of data. it also control overfitting very well in the model.
* Support Vector Machine (SVM)
  Support vector machine is an powerful algorithm which uses hyperplane instead of regression line Logistic regression.
## Model Performance
Boosting Techniques performs so i select all three boosting models and stack them to get generalize output.<br>
* XGBoost cross accuracy: 78.54%
* Decision Tree accuracy: 72.99%
* Gradient Boosting accuracy: 79.77%
* LGBM accuracy: 78.88%
* Random Forest cross validation accuracy score is : 78.83%
* SVM cross validation accuracy score is : 78.63%
##### After hyperparameter tuning and stacking the models:
Accuracy = 81.26% <br>
Currently we have 7043 rows in data if we increase data we can increase model accuracy.
