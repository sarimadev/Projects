# Read Me

## Project Overview

This project involves analyzing a dataset and fitting a Machine Learning model to predict a continuous target variable, 'y'. This task is a regression problem. It also includes examining the dataset, training a simple Linear Regression model, tuning the model for better performance, and analyzing the conditions of regression for complete interpretability.

## Dataset
The dataset consists of 150 observations with 8 numerical features (x1, x2, x3, ..., x8) and one target variable 'y'.

## Instructions

### Step 1: Load and Analyze the Data

1. The data is loaded from a csv file into a pandas dataframe.
2. The target attribute 'y' is separated from the features (X).
3. The target attribute is analyzed to see that it's a continuous variable.
4. Visualize the frequency distribution of the target variable using a histogram.
5. Inspect the feature data and view the number of rows and columns in the dataset.
6. Show the 5-number summary of the features.

### Step 2: Training and Testing a Machine Learning Pipeline

1. The data is split into training (70%) and testing (30%) sets.
2. A pipeline is created with two stages: StandardScaler and LinearRegression.
3. The pipeline is fitted on the training data, and predictions are made on train and test data.
4. Compute the R-squared score to evaluate the performance of the model on both training and testing sets.

### Step 3: Tuning the Machine Learning Pipeline

1. The data is split into tuning (70%) and validation (30%) sets.
2. Use nested K-Fold cross-validation to evaluate the model for each degree of the polynomial features.
3. Find the best degree for PolynomialFeatures.
4. Evaluate the final model's performance on the unseen validation set using the best hyperparameters from the tuning phase.
5. Compute the R-squared score to evaluate the performance of the model on both tuning and validation sets.

### Step 4: Model Interpretation

1. Create a dataframe with the actual values, predicted values and residuals on the best model, which uses the validation data.
2. Check the normality of residuals.
3. Check for the independence of residuals(Homoscedasticity) by plotting a scattered plot to explore the relationship of residuals between actual and predicted values.

## Requirements

- Python 3.7 or above
- Libraries: pandas, sklearn, seaborn, matplotlib, numpy, warnings

## How to Run

1. Download the data.csv file and place it in your project directory.
2. Run the provided Python script.

## Results

The R-squared values of our initial model were significantly lower than the R-squared values of the tuned model, indicating that the initial model was underfitting the data. After the tuning process, we achieved a higher R-squared score and better bias-variance tradeoff.

## Limitations

This model is based on Linear Regression, which assumes a linear relationship between input and output variables. Although we incorporated PolynomialFeatures to capture potential non-linearity, complex datasets with non-linear relationships may not be well-modelled using this approach.
