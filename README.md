# Titanic Dataset Analysis and Survival Prediction

## Overview

This project analyzes the Titanic dataset to uncover insights about passenger survival and builds predictive models to estimate the likelihood of survival. The dataset provides information about passengers on board the RMS Titanic, including their demographics, ticket class, cabin information, and survival outcomes.

The project involves data exploration, feature engineering, data preprocessing, model building, and model evaluation. It aims to answer questions about the factors that influenced passenger survival and demonstrates the use of various machine learning algorithms for classification tasks.

## Project Structure

The project is structured as follows:

1. **Data Loading and Initial Exploration**:
   - The project begins by loading the training and test datasets and displaying the initial data to gain an understanding of its structure.

2. **Data Exploration**:
   - Exploratory data analysis (EDA) is performed on both numeric and categorical data.
   - Histograms, correlation plots, and pivot tables are used to visualize data distributions and relationships with survival.

3. **Feature Engineering**:
   - New features are created based on existing columns to extract valuable information from the dataset.
   - Features like 'cabin_multiple,' 'cabin_adv,' 'numeric_ticket,' and 'name_title' are engineered to enhance model performance.

4. **Data Preprocessing for Model**:
   - Missing values are handled by imputing the mean for 'Age' and 'Fare' and dropping rows with missing 'Embarked' values.
   - Feature scaling, normalization, and one-hot encoding are performed to prepare the data for machine learning models.

5. **Model Building and Evaluation**:
   - Multiple machine learning models, including Gaussian Naive Bayes, Logistic Regression, Decision Tree, K-Nearest Neighbors, Random Forest, Support Vector Classifier, and XGBoost, are built and evaluated.
   - Cross-validation is used to assess model performance, and mean accuracy scores are calculated for each model.

6. **Voting Classifier**:
   - A voting classifier is created to combine predictions from multiple models using a "soft" voting strategy.
   - The voting classifier aggregates results from Logistic Regression, K-Nearest Neighbors, Random Forest, Gaussian Naive Bayes, Support Vector Classifier, and XGBoost.

7. **Preparing Test Data for Prediction**:
   - Columns present in the training data but not in the test data are identified (columns_not_in_test).
   - A new DataFrame (X_test_new) is created for the test data, ensuring that it contains all necessary columns and fills missing ones with zeros.

8. **Model Prediction and Submission**:
   - The voting classifier is fitted on the training data, and predictions are made on the prepared test data (X_test_new).
   - Predictions are saved to a CSV file for submission.
