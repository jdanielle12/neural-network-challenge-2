# Employee Attrition and Department Prediction

## Project Overview
This project focuses on predicting employee attrition and department using a multi-output neural network. The dataset comprises various attributes of employees, such as age, daily rate, distance from home, education, job satisfaction, and more. The neural network shares hidden layers between two output branches: one for predicting employee attrition and the other for predicting the department.

## Table of Contents
1. Introduction
2. Data Preprocessing
3. Model Architecture
4. Training the Model
5. Evaluation
6. Usage
7. Summary

## Introduction
Employee attrition is a critical issue for many organizations, impacting productivity and morale. This project leverages a neural network to predict which employees might leave and which department they belong to. By accurately predicting attrition and department, organizations can take proactive measures to retain talent and manage departmental dynamics more effectively.

## Data Preprocessing
1. **Import the Data**
The dataset is imported from a CSV file `https://static.bc-edx.com/ai/ail-v-1-0/m19/lms/datasets/attrition.csv`, which contains various attributes of employees.

2. **Create the Target DataFrame**
We create a target DataFrame (`y_df`) that includes columns for attrition and department. These will be the outputs of our neural network. 

3. **Select Features for Prediction**
Ten relevant features are chosen for the input DataFrame (`X_df`). These features include age, daily rate, distance from home, education, environment satisfaction, job satisfaction, monthly income, number of companies worked, total working years, and years at the company.

4. **Data Types**
We ensure that the selected features are of the appropriate data types. This step is crucial for the model to process the data correctly. 

5. **Split the Data**
The data is split into training and testing sets. This allows us to train the model on one subset of data and evaluate its performance on another, ensuring that the model generalizes well to unseen data.

6. **Encode Categorical Data**
While the selected features are numeric, the target columns (attrition and department) need encoding. Attrition is encoded as binary values (0 for No, 1 for Yes), and the department is label-encoded to numeric values.

7. **Scale the Features**
Feature scaling is performed to standardize the range of the independent variables. This step helps improve the convergence speed and performance of the neural network.

## Model Architecture
