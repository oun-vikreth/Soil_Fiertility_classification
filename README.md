# Soil Fertility Prediction Report

## Introduction
This report presents the process and results of a machine learning project aimed at predicting soil fertility. The dataset used in this project contains various soil properties such as Nitrogen (NH4+), Phosphorous (P), Potassium (K), soil acidity (pH), electrical conductivity, organic carbon, sulfur (S), Zinc (Zn), Iron (Fe), Copper (Cu), Manganese (Mn), and Boron (B). The target variable is the class of fertility, which can be "Less Fertile", "Fertile", or "Highly Fertile".

## Exploratory Data Analysis (EDA)
The EDA started with loading the dataset and checking the first few rows to understand the data structure. The dataset was then checked for missing values, and descriptive statistics were calculated to get a sense of the data distribution. 

A count plot was created to visualize the distribution of the target variable, 'Output'. Box plots were also created for each numerical variable to check for outliers and understand their relationship with the target variable. 

A correlation matrix heatmap was generated to understand the relationships between the different features. It was observed that 'N' (Nitrogen content) had the highest correlation with 'Output' (soil fertility).

## Data Preprocessing
The data was split into features (X) and target (y). The features and target were then split into training and test sets, with 80% of the data used for training and 20% used for testing. The feature data was scaled using the StandardScaler from sklearn.

## Model Fitting
Three different models were trained on the data: RandomForestClassifier, SVM, and GradientBoostingClassifier. The performance of each model was evaluated using a classification report, which provides precision, recall, f1-score, and support for each class.

## Results
The RandomForestClassifier achieved an accuracy of 89%, the SVM achieved an accuracy of 84%, and the GradientBoostingClassifier achieved an accuracy of 85%. 

## Conclusion
This project demonstrated the application of machine learning for predicting soil fertility based on various soil properties. The RandomForestClassifier performed the best among the three models used. Future work could involve tuning the hyperparameters of the models, trying other models like XGBoost or LightGBM, or using ensemble methods to potentially improve the accuracy of the predictions.
