# Neural Network Charity Analysis

## Overview

Alphabet Soup is looking to create a machine learning and neural network capable of predicting applicant success if funded by the company. With data on over 34,000 organization in years past, we will create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results

### Data Pre-Processing
 - Model Target Variables: "IS_SUCCESSFUL" column is used as the y value to determine where or not the funds were used successfully
 - Model Features Variables: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMOUNT', and 'INCOME_AMOUNT'
 - Model Features Elimination: 'EIN' and 'Name' were remvoed as they are not useful data for this model

### Optimitizations
 - Optimization 1: Increased the class_counts < value from 1800 to 2000 reducing the number of classification values from 6 to 4. With optimization, the Accuracy Score dropped from 0.7291 to 0.7268. Therefore the class_count will be reset back to 1800 before the next optimization
 - Optimization 2: In this optimization, I added a third hidden layer with 15 nodes in order to allow for a more granular representation of the data. Unfortunately, this update was only able to increase the accurancy score to 0.7293, only a slight improvement over the original data.
 - Optimization 3: In order to see increased accuracy, we gave the mode an additional hidden layer (fourth layer), increased nodes for second and third layers, and increased the epochs from 100 to 200. While this doubled the amount of time it took for our code run, we did see accuracy improve to 0.7303.

Unfortunately, the optimizations made did not result in achieveing our goal of 75%. Future optimizations we can try are to add additiionl hidden layers. 

## Summary
Increasing the number of hidden layers might improve the accuracy or might not, it really depends on the complexity of the problem. The more hidden layers the model has, the "deeper" the deep learning can go. Increasing our epoch helps to ensure that we are not underfitting our data, but cautious must be used to ensure we do not overfit the data as well. 
