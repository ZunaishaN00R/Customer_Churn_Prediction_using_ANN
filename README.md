# Customer Churn Prediction using Neural Networks
## Overview
This repository contains code for predicting customer churn using a neural network implemented with TensorFlow and Keras. The dataset used for training and testing the model is stored in a CSV file named 'customer_churn.csv'.

## Dataset
The dataset consists of customer information, including features such as gender, senior citizen status, partner, dependents, tenure, phone service, multiple lines, internet service, online security, online backup, device protection, tech support, streaming TV, streaming movies, contract type, paperless billing, payment method, monthly charges, total charges, and the target variable 'Churn' indicating whether a customer has churned or not.

## Preprocessing
1. The 'customerID' column is dropped as it does not contribute to the prediction.
2. The 'TotalCharges' column is converted from object type to float64 using pandas' `pd.to_numeric()` function.
3. Leading and trailing spaces in categorical columns are removed to ensure consistency.

## Data Visualization
Data visualization is performed using matplotlib and seaborn to understand the distribution of features. Two histograms are plotted for 'tenure' and 'monthly charges', showing the distribution of values for customers who churned and those who did not.

## Encoding
Label encoding is applied to the 'Churn' column using scikit-learn's `LabelEncoder` to convert it into numerical format (0 for 'No' and 1 for 'Yes').

## Train-Test Split
The dataset is split into training and testing sets using scikit-learn's `train_test_split` function.

## Model
A neural network model is implemented using TensorFlow and Keras. Three different architectures are explored:
1. Relu activation function with binary cross-entropy loss.
2. Relu activation function with mean squared error loss.
3. Sigmoid activation function with mean squared error loss.

## Results
The models are trained and evaluated, and the accuracy scores are reported. Model predictions are also obtained for the test set.

Feel free to explore and experiment with different architectures and hyperparameters for further improvement.
