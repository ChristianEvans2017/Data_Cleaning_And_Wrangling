# Titanic: Data Cleaning, Wrangling, and Feature Engineering

This project focuses on cleaning, wrangling, and feature engineering analysis of the Titanic dataset from Kaggle. Key aspects of this project include filling missing values, creating new features to improve survival prediction performance, and analyzing the structure and relationships within the dataset.

## Project Overview

**1. Data Cleaning and Wrangling Steps:**

The project consists of several cleaning and wrangling steps, including:

- Loading the data and inspecting the initial training set
- Computing unique value counts for categorical features
- Creating new features (Fare_PerPassenger, NameTitle, and NumFamily)
- Identifying and handling missing values for Age, Embarked, CabinLetter, CabinLetter_Cohort, CabinNumber, and CabinNumber_Group
- Encoding categorical variables (Sex and NameTitle)
- Estimating missing Age values using various regression models (Linear Regression, Decision Tree Regression, Random Forest Regression) and encoding strategies (Dummy Variable Encoding and Smoothed Target Encoding)
- Predicting missing CabinLetter_Cohort and CabinNumber_Group values using various classification models (Decision Tree Classifier, Random Forest Classifier, Gradient Boosting Classifier, Ensemble Classifier)

**2. Prediction Models Summary:**

The prediction models used in this project include:

- Age Prediction: Random Forest Regression with Smoothed Target Encoding gave the best performance in terms of bias-variance trade-off and improvement with more data.
- CabinLetter_Cohort Prediction: Both the Decision Tree Classifier and the Ensemble Classifier provided good balance between performance and consistency. Although the Decision Tree Classifier achieved the highest performance score, the Ensemble Classifier offered more reliable results on new data.
- CabinNumber_Group Prediction: None of the candidate models performed well on this classification task, despite hyperparameter tuning. Therefore, missing CabinNumber_Group values were left as null values.

**3. Training Set Dataframe Before and After Cleaning:**

*Before Cleaning:*
- 891 rows x 11 columns (Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked)
- Missing values in Age, Cabin, and Embarked

*After Cleaning:*
- 891 rows x 22 columns (Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked, Ticket_Count, Fare_PerPassenger, NameTitle, NumFamily, CompleteInfo, CabinLetter, CabinNumber, CabinLetter_Cohort, CabinLetter_Cohort_DT, CabinLetter_Cohort_ECLF, CabinNumber_Group)
- Original missing values filled in Age and Embarked, but Cabin still has missing data
- Additional columns added for new features and predictions

This Markdown file serves as an overview of the Titanic dataset cleaning and wrangling project, explaining the steps followed, summarizing the prediction model performances, and providing a before-and-after cleaning description of the training set dataframe. The project demonstrates the user's proficiency in data cleaning, wrangling, and feature engineering, utilizing various machine learning models to fill missing values and create new features that improve the overall understanding and prediction performance on the Titanic dataset.

## Data Visualizations

Several visualizations are created within the notebook using Matplotlib. I've added a screenshot of each to this repository:

- Survival Rates for Passengers with and without Missing Feature Values: CompleteInfo_Survival_Rates.png
- Regression Learning Curve Analysis: Age_Prediction_Learning_Curves.png
- Classification Prediction Score Analysis (CabinLetter_Cohort): CabinLetter_Cohort_Prediction_Scores.png
- Survival Rates for Cabin Numbers: CabinNumber_Survival_Rates.png
- Survival Rates for CabinNumber_Group Values: CabinNumber_Group_Survival_Rates.png
- Classification Prediction Score Analysis (CabinNumber_Group): CabinNumber_Group_Prediction_Scores.png

## Contact

I appreciate your feedback and suggestions! Feel free to fork this project and edit as you please. If you'd like to pass along any suggestions, you can contact me at christianevans0226@gmail.com!

