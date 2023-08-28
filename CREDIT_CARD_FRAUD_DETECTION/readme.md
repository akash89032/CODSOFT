# Credit Card Fraud Detection

This repository contains a credit card fraud detection project that uses logistic regression as the classification algorithm and the SMOTE (Synthetic Minority Over-sampling Technique) for handling imbalanced data.

## Table of Contents

- [Dataset](#dataset)
- [Project Overview](#project-overview)
  - [Data Preprocessing](#data-preprocessing)
  - [Data Balancing with SMOTE](#data-balancing-with-smote)
  - [Logistic Regression Models](#logistic-regression-models)
- [Model Evaluation](#model-evaluation)
- [Model Selection](#model-selection)
- [Usage](#usage)

## Dataset

The dataset used for this project is the "creditcard.csv" dataset. It contains credit card transactions made by European cardholders in September 2013. The dataset consists of transactions that occurred over two days, with a total of 284,807 transactions. Out of these transactions, there are 492 fraud cases, making it a highly imbalanced dataset. The positive class (frauds) represents only 0.172% of all transactions.

**Dataset Source:** [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)

Due to confidentiality reasons, the input variables in the dataset are transformed into numerical features using PCA (Principal Component Analysis) transformations.

## Project Overview

### Data Preprocessing

Data preprocessing is a crucial step in preparing the dataset for modeling. In this project, the following data preprocessing techniques were applied:

- **Scaling**: The features in the dataset were scaled to have a mean of 0 and a standard deviation of 1. This step ensures that all features have the same scale, which is important for logistic regression.

- **Train-Test Split**: The dataset was divided into a training set and a testing set to evaluate model performance. Common practice is to use a 70-30 or 80-20 split, with most of the data used for training.

### Data Balancing with SMOTE

To address the class imbalance problem, the SMOTE (Synthetic Minority Over-sampling Technique) was employed. SMOTE generates synthetic examples of the minority class to balance the dataset and prevent the model from being biased toward the majority class.

#### What is SMOTE?

SMOTE is a powerful technique used in machine learning for handling imbalanced datasets. It works by creating synthetic samples from the minority class by interpolating between existing samples. This helps in achieving a balanced dataset and improving the model's ability to detect minority class instances.

### Logistic Regression Models

Four logistic regression models were implemented:

1. **Logistic Regression (Before Balancing Data):**
   - This model used logistic regression on the imbalanced dataset without any oversampling techniques.
   - Performance metrics were evaluated, including precision, recall, and F1-score.

2. **Logistic Regression with Optimal C Value (Before Balancing Data):**
   - Similar to the first model, logistic regression was applied to the imbalanced dataset.
   - The optimal C value was selected to fine-tune the model.
   - Performance metrics were evaluated and compared with the baseline model.

3. **Logistic Regression (After Balancing Data with SMOTE):**
   - After applying SMOTE to balance the data, logistic regression was applied again.
   - Performance metrics were assessed on the balanced dataset.

4. **Logistic Regression with Optimal C Value (After Balancing Data with SMOTE):**
   - Logistic regression was applied to the balanced dataset with the optimal C value.
   - Performance metrics were evaluated and compared with the other models to assess improvements.

## Model Evaluation

The models were evaluated based on various metrics, including precision, recall, and F1-score. The ROC score was also used to assess model performance.

## Model Selection

After comparing the performance of all four models, the logistic regression model with the optimal C value after balancing the data with SMOTE emerged as the preferred choice. This decision was based on the following factors:

- ROC score of 0.99 on the train set and 0.97 on the test set for the logistic regression model after SMOTE.
- Simplicity and ease of interpretation of the logistic regression model.

## Usage

To run the code in this repository, follow these steps:

1. Download the "creditcard.csv" dataset from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud) and place it in the same directory as the code.

2. Install the necessary Python libraries specified in the `requirements.txt` file.

3. Run the Jupyter Notebook or Python script provided to train and evaluate the logistic regression models.

---
Feel free to reach out with any questions or improvements to this project. Thank you for your interest!
