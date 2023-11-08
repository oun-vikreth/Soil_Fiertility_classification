<p align="center">
<img  src="https://d17ocfn2f5o4rl.cloudfront.net/wp-content/uploads/2023/07/BP-AI-in-Agriculture-The-Future-of-Farming_body-im-8.jpg" alt="my banner">
</p> 



# Soil Fertility Classification

## Introduction
This notebook is a small part of our full project. It just presents some of the process and results of a machine learning project aimed at predicting soil fertility. The dataset used in this project contains various soil properties such as Nitrogen (NH4+), Phosphorous (P), Potassium (K), soil acidity (pH), electrical conductivity, organic carbon, sulfur (S), Zinc (Zn), Iron (Fe), Copper (Cu), Manganese (Mn), and Boron (B). The target variable is the class of fertility, which can be "Less Fertile", "Fertile", or "Highly Fertile".

## Exploratory Data Analysis (EDA)
The EDA started with loading the dataset and checking the first few rows to understand the data structure. The dataset was then checked for missing values, and descriptive statistics were calculated to get a sense of the data distribution. 

A count plot was created to visualize the distribution of the target variable, 'Output'. Box plots were also created for each numerical variable to check for outliers and understand their relationship with the target variable. 

A correlation matrix heatmap was generated to understand the relationships between the different features. It was observed that 'N' (Nitrogen content) had the highest correlation with 'Output' (soil fertility).

## Data Preprocessing
The data was split into features (X) and target (y). The features and target were then split into training and test sets, with 80% of the data used for training and 20% used for testing. The feature data was scaled using the StandardScaler from sklearn.

## Model Fitting

### RandomForestClassifier
The RandomForestClassifier is a meta-estimator that fits a number of decision tree classifiers on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting. The sub-sample size is controlled with the `max_samples` parameter if `bootstrap=True` (default), otherwise the whole dataset is used to build each tree. It's a powerful model that works well on large datasets and has the ability to handle a mixture of features (binary, categorical, numerical), but it can be prone to overfitting, especially with noisy data.

### Support Vector Machine (SVM)
Support Vector Machine (SVM) is a powerful and flexible class of supervised algorithms for both classification and regression. It uses a technique called the kernel trick to transform your data and then based on these transformations it finds an optimal boundary between the possible outputs. SVMs are well suited for classification of complex but small- or medium-sized datasets. However, they do not scale well to large datasets and do not directly provide probability estimates.

### GradientBoostingClassifier
Gradient Boosting Classifier is a machine learning technique for regression and classification problems, which produces a prediction model in the form of an ensemble of weak prediction models, typically decision trees. It builds the model in a stage-wise fashion like other boosting methods do, and it generalizes them by allowing optimization of an arbitrary differentiable loss function. Gradient boosting is typically used with decision trees (especially CART trees) of a fixed size as base learners. It's a powerful model with good performance but can be prone to overfitting and requires careful tuning of different hyperparameters.

Each of these models has its strengths and weaknesses, and their performance will depend on the specifics of the data and the task at hand. It's always a good idea to try a variety of models and select the one that performs best on your validation data.

Three different models were trained on the data: RandomForestClassifier, SVM, and GradientBoostingClassifier. The performance of each model was evaluated using a classification report, which provides precision, recall, f1-score, and support for each class.

## Results

| Model                     | Accuracy (%) |
|---------------------------|--------------|
| RandomForestClassifier    | 89           |
| Support Vector Machine    | 84           |
| GradientBoostingClassifier| 85           |

## Conclusion
This project demonstrated the application of machine learning for predicting soil fertility based on various soil properties. The RandomForestClassifier performed the best among the three models used. Future work could involve tuning the hyperparameters of the models, trying other models like XGBoost or LightGBM, or using ensemble methods to potentially improve the accuracy of the predictions.


