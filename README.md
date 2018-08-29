# Kaggle-House-Credit-Default-Risk
Worked on kaggle House credit default risk competition to predict how capable applicant is of repaying a loan
**Summary**: Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience, Home Credit makes use of a variety of alternative data--including telco and transactional information--to predict their clients' repayment abilities. Details of project can be find here : https://www.kaggle.com/c/home-credit-default-risk

**Data Description** : 

1) **application_{train|test}.csv**:
This is the main table, broken into two files for Train (with TARGET) and Test (without TARGET).
Static data for all applications. One row represents one loan in our data sample.

2) **bureau.csv**:
All client's previous credits provided by other financial institutions that were reported to Credit Bureau (for clients who have a loan in our sample).
For every loan in our sample, there are as many rows as number of credits the client had in Credit Bureau before the application date.

3)**bureau_balance.csv**:
Monthly balances of previous credits in Credit Bureau.
This table has one row for each month of history of every previous credit reported to Credit Bureau – i.e the table has (#loans in sample * # of relative previous credits * # of months where we have some history observable for the previous credits) rows.

4)**POS_CASH_balance.csv**:
Monthly balance snapshots of previous POS (point of sales) and cash loans that the applicant had with Home Credit.
This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample – i.e. the table has (#loans in sample * # of relative previous credits * # of months in which we have some history observable for the previous credits) rows.

5)**credit_card_balance.csv**:
Monthly balance snapshots of previous credit cards that the applicant has with Home Credit.
This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample – i.e. the table has (#loans in sample * # of relative previous credit cards * # of months where we have some history observable for the previous credit card) rows.

6)**previous_application.csv**:
All previous applications for Home Credit loans of clients who have loans in our sample.
There is one row for each previous application related to loans in our data sample.

7)**installments_payments.csv**:
Repayment history for the previously disbursed credits in Home Credit related to the loans in our sample.
There is a) one row for every payment that was made plus b) one row each for missed payment.
One row is equivalent to one payment of one installment OR one installment corresponding to one payment of one previous Home Credit credit related to loans in our sample.

8)**HomeCredit_columns_description.csv**:
This file contains descriptions for the columns in the various data files.
Rest of the details can be find here: https://www.kaggle.com/c/home-credit-default-risk/data

**Work Done**:
After doing the merging, feature engineering and data cleaning, used Hyperopt package for implementing sequential based hyperparameters tuning method. Details of Sequential based optimization can be find here: https://towardsdatascience.com/an-introductory-example-of-bayesian-optimization-in-python-with-hyperopt-aae40fff4ff0.
Also, used permutation importance method for feature selection as mentioned here:https://academic.oup.com/bioinformatics/article/26/10/1340/193348
and also get information using the kernel:https://www.kaggle.com/ogrellier/feature-selection-with-null-importances
