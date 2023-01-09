# Rossmann-Sales-Prediction

## Abstract
Forecast prediction is a process of predicting a future value using past data and some other related factors. If we want to forecast the present day sales or future sales using past sales and some other related factors like seasonality, festivals, economic conditions etc. then it is known as Sales forecasting. 
We can use different methods for Sales forecasting. Among them, one of the most robust methods is Sales forecasting using machine learning algorithms.
In this method, we preprocess all the input to machine-understandable features and then apply a machine learning algorithm on top of it.

## Problem Statement
Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.

We are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

## Introduction
Demand for product or service is not constant, it changes with respect to time. But to maintain the demand and supply balance it is very important to understand the demand of product or service in the future.
Sales prediction is a process of estimating demand of sales of a particular product or service over a period of time.      
Sales prediction not only helps in balancing the supply chain but also helps in making future business strategies like budgets, hiring, incentives, goals, acquisitions and various other growth plan.

## Exploratory data analysis
1) Analysing the basic information of the dataset like number of observations and features, data Type of different features, null values of each feature.
2) Day of the week has a negative correlation indicating low sales as the weekends, and promo, customers and open has positive correlation.
3) State Holiday has a negative correlation suggesting that stores are mostly closed on state holidays indicating low sales.
4) CompetitionDistance showing negative correlation suggests that as the distance
increases sales reduce, which was also observed through the scatterplot earlier.
5) There's multicollinearity involved in the dataset as well. The features telling the
same story like Promo2, Promo2 since week and year are showing multicollinearity.

## Data Manipulation and Feature Engineering
1) Data manipulation involves manipulating and making necessary changes in our dataset before deploying it into machine learning algorithm.
2) Extracting current date, month, year, week number from date column.
3) Since there is no sale when the shops are closed, we removed all the observations when the store is closed.
4) Combine CompetitionOpenSinceMonth, CompetitionOpenSinceYear to give "competition_open” which tells since how many months competition is open.
5) Combine Promo2SinceWeek, Promo2SinceYear to give "promo_2_open“which tells since how many months the shop is participating in promo2.
6) Getting “IsPromo2Month” from promo_interval_open which tells is Promo2 open for a particular month or not.
7) CompetitionDistance has some null values we will deal with it by filling null values with median of CompetitionDistance.

## Algorithms Used

### Linear Regression
Linear Regression is a machine learning algorithm grounded on supervised learning. It performs a regression task. Regression models a target prediction value grounded on independent variables. It's substantially used for finding out the relationship between variables and prediction. Different regression models differ grounded on – the kind of relationship between dependent and independent variables they're considering, and the number of independent variables getting used.

### Decision Tree
It is the most impressive and well-known ML algorithm for classification and prediction. A Decision tree is a flowchart-like tree structure, where each inner node signifies a test on an attribute, each branch addresses a result of the test, and each leaf node (terminal node) holds a class label.

### Random Forest
Every decision tree has an excessive variance, however, while we integrate them all collectively in parallel then the ensuing variance is low as every selection tree receives perfectly trained on that sample data, and as a result, the output doesn’t rely upon one decision tree however on more than one decision trees. In the case of a classification problem, the final output is taken through the use of majority voting. In the case of a regression problem, the final output is the average of output of different tress.

Random Forest is an ensemble approach able to act each regression and classification with the usage of multiple discussion trees and a method referred to as Bootstrap and Aggregation, generally referred to as bagging.

### Gradient Boosting

Gradient Boosting is an ensemble modelling, approach that tries to construct a robust classifier from the range of weak classifiers.
Gradient Boosting is a famous boosting algorithm. In gradient boosting, every predictor corrects its previous error.
It also supports parallelization (it can generate the different nodes of tree parallel), can use the hardware    resources efficiently through Cache-Awareness, it can also handle sparse data efficiently.

 ## Conclusion

Sales Prediction helps in making future business strategies like budgets, hiring, incentives, goals, acquisitions and various other growth plan. In this project we analyzed more than one thousand stores for sales prediction. After analysing we conclude some important observations as follows

1.	Stores which are running promo have more sales.

2.	The State Holiday affects adversely to sales while school holiday affects positively to sales.

3.	Store type B though being few in number had the highest sales average. The reasons
       include all three kinds of assortments specially assortment level b which is only                                               
       available at type b stores and being open on Sundays as well.

4.	With increase in competition distance sales decrease. This may be because the store with low competition distance indicates that the store is in busy place.


