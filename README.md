# E-Commerce-and-Retail-B2B-Case-Study

## Late Payment Prediction and Customer Segmentation for Schuster

## Project Overview
This project aims to help Schuster, a multinational retail company dealing in sports goods and accessories, understand and predict its vendors' payment behaviors. The goal is to identify vendors likely to make late payments on invoices to enable proactive follow-up and prevent financial impacts. This solution includes data preprocessing, exploratory data analysis (EDA), customer segmentation, and the development of a binary classification model to predict late payments.

## Problem Statement
Schuster faces issues with vendors who frequently delay payments, resulting in financial and time losses. The objective is to:

- Analyze vendors' past payment data to understand payment behavior.
- Segment vendors based on payment behavior patterns.
- Predict the likelihood of delayed payments on open invoices.
- Recommend actions to prioritize collections effectively.

## Data Sources
This project utilizes two primary datasets:

#### Received Payment Data: 
Contains historical data on transactions made with various vendors, including details like payment term, payment date, invoice amount, and due date. This data will be used to create and train the prediction model.
#### Open Invoice Data: 
Contains information about current open invoices where payments are pending. This dataset will be used to test and apply the model in predicting potential late payments.

The data dictionary provides details about the columns in both datasets.

## Approach

### 1. Data Preparation
- Clean and preprocess the Received Payment Data by removing any records with negative invoice values.
- Define a binary target variable to identify if a payment was made on time (0) or late (1), derived by comparing the payment receipt date with the due date.
- Convert Payment Term from text format to a numerical feature by calculating the difference between the due date and invoice creation date.

### 2. Exploratory Data Analysis (EDA)
- Conduct EDA to identify key patterns in the data, such as common payment delays, variations in payment amounts, and average payment times.
- Visualize customer payment behaviors and other critical factors that may contribute to late payments.

### 3. Customer Segmentation
- Segment vendors based on historical payment patterns using clustering techniques, particularly focusing on:
  #### Average Payment Time:
  The average delay (or promptness) in days.
  #### Standard Deviation of Payment Time:
  Variability in the payment delay.
- Use clustering to classify vendors into groups that exhibit similar payment behaviors. These clusters serve as an input feature for the classification model.

### 4. Model Building
- Build and evaluate multiple binary classification models (e.g., Logistic Regression, Decision Trees, Random Forest, etc.) to predict whether an invoice payment will be delayed.
- Identify and select the most significant predictor variables to enhance model performance and explainability.

### 5. Model Application and Prediction
- Apply the selected model on the Open Invoice Data to predict late payments. The model should predict only for records with a negative AGE value (invoices not yet overdue).
- Aggregate predictions at the customer level to provide insights on the likelihood of each customer’s future payment behavior.

### 6. Result Visualization
- Visualize segmentation results and model output using plots and summary tables.
- Provide visual summaries of important predictor variables and segmentation clusters.

## Results and Deliverables
- A Jupyter notebook containing:
  - EDA insights and visualizations.
  - Customer segmentation outputs (clusters and patterns).
  - The final classification model and its evaluation.
  - Predictions on open invoices with an indication of customers likely to make late payments.
- Recommendations for proactive customer follow-up based on the likelihood of delayed payments.
