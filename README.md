# Code README - Data Preprocessing and Classification
This README provides an overview of the Python code that focuses on data preprocessing and classification using various machine learning algorithms. The code is written in Python and utilizes libraries such as pandas, numpy, matplotlib, seaborn, and scikit-learn.

## Objective
The primary goal of this code is to demonstrate the process of preprocessing a dataset and then applying classification algorithms to predict the "TenYearCHD" (Ten-Year Risk of Coronary Heart Disease) binary outcome variable.

## Code Structure
Import Libraries and Read Data:

Import necessary libraries such as pandas, numpy, matplotlib, seaborn.
Read the dataset "framingham.csv" using pandas and display the first few rows.
Handling Missing Values:

Display information about the dataset using data.info().
Display descriptive statistics using data.describe().
### Handle missing values for specific columns:
- "education" column: Replace missing values with the most frequent value (1.0).
- "cigsPerDay" column: Replace missing values with 0.0 and treat outliers (>50) with a capped value of 50.
- "BPMeds" column: Replace missing values with 0.0.
- "totChol", "BMI", "heartRate" columns: Replace missing values with the mean of respective columns.
- "glucose" column: Replace missing values with a predefined value (75.0).
- Visualize the distribution of "glucose" using a histogram.
## Data Visualization:

Create a histogram and scatter plot to visualize the distribution of "glucose" and the relationship between "sysBP" and "TenYearCHD," respectively.
### Data Balancing:

Check the balance of the "TenYearCHD" classes using a bar plot.
Apply Synthetic Minority Over-sampling Technique (SMOTE) to balance the dataset.
Display the count of labels before and after SMOTE.
### Feature Selection:

Utilize backward elimination using Ordinary Least Squares (OLS) regression from statsmodels to select relevant features.
Print the number of selected features.
### Split Data:

Split the dataset into training and testing sets using train_test_split from scikit-learn.
### Classification:

- Implement Naive Bayes and XGBoost classifiers.
- Train the Gaussian Naive Bayes classifier on the training data.
- Predict the classes on the test data and calculate the accuracy scores for both training and testing sets.
- Train an XGBoost classifier on the training data.
- Calculate the accuracy scores for the XGBoost classifier on both training and testing sets.
## Usage
Make sure you have Python and required libraries installed.
Place the dataset "framingham.csv" in the same directory as the script.
Run the script in your preferred Python environment.
## Note
This code is for educational and illustrative purposes. Depending on your specific use case, you might need to customize the preprocessing steps, choose appropriate algorithms, and perform hyperparameter tuning to achieve better results.
Remember to consider ethical implications and best practices when using machine learning algorithms for real-world applications.




