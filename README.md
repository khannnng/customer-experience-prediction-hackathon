# Customer experience prediction hackathon

### About the competition
Data Science hackathon as part of the [professional program in Data Science/Machine Learning by GreatLearning and MIT IDSS](https://olympus.mygreatlearning.com/eportfolio).

### Problem statement:
The goal of the problem is to predict whether a passenger was satisfied or not considering his/her overall experience of traveling on the Shinkansen Bullet Train.

The objective of this problem is to understand which parameters play an important role in swaying passenger feedback towards a positive scale. You are provided test data containing the travel data and the survey data of passengers. Both the test data and the train data are collected at the same time and belong to the same population.

### Project walkthrough
- 1/ [Data quality check](https://github.com/khannnng/customer-experience-prediction-hackathon/blob/main/1.%20EDA%20%2B%20Fill%20null.ipynb)
Main issue with the data was that it is multiple survey results of different customer segments slammed together, each has their own participating criteria, resulted in many missing values if they were not included in the survey.

- 2/ [Missing values imputation](https://github.com/khannnng/customer-experience-prediction-hackathon/blob/main/2.0%20KNNImputing.ipynb)
Selectively fill missing values with similar rating categories based on how correlated the two ratings are. For numerical variables, the values was filled by KNN imputer. 
  
- 3,4,5/ Base models + hyperparameter tuning
Experiment with different feature selections, feature engineering, scaler, models,... . Random forest and XGB has the most promising result and was selected for further tuning.
It takes relatively short time to build a model with around 90% ~ 95% accuracy but it was really hard to break through that.

- 6/ ANN models + hyperparameter tuning
Training ANN models took the most time and left for last, once I exhausted all other models. Hyperparameter tuning is harder too, since there are multiple parameters like number of layers, neuron in each layer, activation function, dropout, learning rate, batch size to tune. In the end, ANN surpassed XGB by a very small margin (maybe around 0.01%) yet that was enough to secure the 3rd place on the leaderboard.

![image](https://github.com/khannnng/customer-experience-prediction-hackathon/assets/112837341/da5f7234-e7ec-4efa-9a31-99ce0984b82a)

