# Credit Risk Classification Challenge

## Background
Credit risk classification presents a significant challenge due to the inherent imbalance in the dataset, where healthy loans significantly outnumber risky loans. This challenge involves using various techniques to train and evaluate models on imbalanced classes. The dataset comprises historical lending activity from a peer-to-peer lending services company, and the objective is to build a model that identifies borrowers' creditworthiness.

## What You’re Creating
You will leverage the `imbalanced-learn` library to train a logistic regression model on two versions of the dataset: the original dataset and a resampled version using the `RandomOverSampler` module from `imbalanced-learn`.

For both datasets, you will:
- Count the target classes
- Train a logistic regression classifier
- Calculate the balanced accuracy score
- Generate a confusion matrix
- Produce a classification report

Additionally, you will document a credit risk analysis report based on a provided template.

## Files
To get started, download the following:

- Module 12 Challenge files

## Instructions
The instructions are divided into the following sections:

### Split the Data into Training and Testing Sets
1. Open the starter code notebook.
2. Read `lending_data.csv` from the Resources folder into a Pandas DataFrame.
3. Create the labels set (`y`) from the “loan_status” column and the features set (`X`) from the remaining columns.
   - Note: A value of 0 in the “loan_status” column indicates a healthy loan, while 1 indicates a high-risk loan.
4. Check the balance of the labels using the `value_counts` function.
5. Split the data into training and testing datasets using `train_test_split`.

### Create a Logistic Regression Model with the Original Data
1. Fit a logistic regression model using the training data (`X_train` and `y_train`).
2. Predict the labels for the testing data using `X_test` and the trained model.
3. Evaluate the model’s performance:
   - Calculate the accuracy score.
   - Generate a confusion matrix.
   - Print the classification report.
4. Answer: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

### Predict a Logistic Regression Model with Resampled Training Data
To potentially improve model performance, you will resample the training data using `RandomOverSampler`:
1. Resample the data with `RandomOverSampler` to ensure equal numbers of labels.
2. Fit the `LogisticRegression` classifier on the resampled data and make predictions.
3. Evaluate the model’s performance:
   - Calculate the accuracy score.
   - Generate a confusion matrix.
   - Print the classification report.
4. Answer: How well does the logistic regression model, trained with oversampled data, predict both the 0 (healthy loan) and 1 (high-risk loan) labels?
