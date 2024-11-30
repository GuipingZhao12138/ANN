# ANN
Neural Network Model for Income Prediction
This repository contains the Python implementation and report for our group project, which developed a neural network model to predict individuals' likelihood of earning above $50,000 based on demographic and socioeconomic data. The analysis and results are based on data from the U.S. Census Bureau.

Project Overview
The objective of this project is to explore and analyze demographic characteristics to predict income levels. Using machine learning techniques, specifically artificial neural networks (ANNs), we built and optimized a model to achieve high predictive accuracy while addressing data preprocessing challenges and ensuring feature alignment.

Key Features:
Prediction Goal: Classify whether an individual's income is ≤ $50,000 or > $50,000.
Performance: Final model accuracy of 84.944% after hyperparameter optimization.
Significant Predictors: Key factors influencing income predictions include:
Capital gain
Relationship status
Educational attainment
Occupational field
Data Preprocessing
Before training the model, the dataset was processed to ensure data quality and compatibility with the neural network:

Missing Values: Imputed missing values for categorical variables with the mode.
Feature Scaling: Applied Min-Max scaling to normalize continuous variables.
Dummy Variables: Converted categorical features into dummy variables to facilitate neural network processing.
Feature Alignment: Ensured test and training datasets had identical feature sets by adding missing columns with zero values.
Neural Network Configuration
The final ANN architecture was optimized through cross-validation, yielding the following configuration:

Input Layer: 96 features
Hidden Layer: 32 neurons with Sigmoid activation
Output Layer: Binary classification using a Sigmoid function
Optimizer: Stochastic Gradient Descent (SGD)
Learning Rate: 0.01
Epochs: 40
Batch Size: 100
Results and Insights
Model Accuracy: 84.944%
False Negative Rate: 10.66% (tends to underpredict higher incomes)
False Positive Rate: 4.86%
Key Insights:
Higher education (e.g., Bachelor’s, Master’s) and professional roles correlate strongly with higher income.
Married individuals and those with significant capital gains are more likely to earn above $50,000.
Limitations and Future Improvements
The model exhibits a class imbalance, leading to a higher false negative rate.
Future iterations could implement techniques like SMOTE for class balancing or ensemble models to further improve accuracy and fairness.
Authors
This project was completed by Guiping Zhao.


