# Data Cleaning and Wrangling of Kaggle's Titanic Dataset

In this project, I showcase my data cleaning and wrangling skills on the Titanic dataset from Kaggle.com. The ultimate goal of the Kaggle competition is to predict the survivors of the Titanic disaster based on the labeled training set. In this project, I focus on cleaning and preparing the provided dataset for usage in a machine learning model.

The project primarily consists of three main tasks:
1. Feature Transformation
2. Feature Imputation
3. Feature Engineering

# A First Look at the Training Set

The original training set of Titanic Dataset consisted of the following columns:

- Survived
- Pclass
- Name
- Sex
- Age
- SibSp
- Parch
- Ticket
- Fare
- Cabin
- Embarked

# Conclusion and Changes Made to Dataset Features

After performing data cleaning and wrangling, the following modifications were made to the dataset:

1. Sex: Transformed into numerical binary values (0 for Male, 1 for Female)
2. Age: Imputed missing values using Random Forest Regressor
3. Embarked: Imputed missing values by taking the mode of the feature
4. NameTitle: Extracted honorific titles from Name feature
5. CompleteInfo: Engineered to indicate if an entry had missing values prior to data wrangling
6. CabinLetter: Extracted letter(s) from Cabin feature
7. CabinNumber: Extracted number(s) from Cabin feature
8. CabinLetter_Cohort: Imputed missing values using a Gradient Boosting Classifier and transformed into numerical values
9. CabinNumber_Group: Imputed missing values using a Random Forest Classifier

These modified features will be used in the subsequent machine learning model to train and predict the outcomes of Titanic passengers.

# Models and Evaluation Methodologies

To predict missing values in the dataset, I employed an array of candidate models and evaluated their performance for high-quality predictions in both the training and test sets. Here is a summary of the prediction models and evaluation methodologies used:

- Regression: Missing Age values were predicted using Linear Regression, Decision Tree Regression, and Random Forest Regression models. Grid search CV was employed for hyperparameter tuning. The best performance was observed using Random Forest Regression with Smoothed Target Encoding.

- Classification: Missing CabinLetter_Cohort and CabinNumber_Group values were predicted using classification methods that included accuracy, precision, recall, and F1 scores. The Gradient Boosting Classifier performed best for CabinLetter_Cohort, while the Random Forest Classifier was chosen for CabinNumber_Group.

Moreover, I utilized a 95% Confidence Interval and Chi-Squared Significance tests to make inferences and test hypotheses about the data.

In conclusion, this project emphasizes the importance of thorough data preprocessing. Data cleaning and wrangling play a crucial part in the success of subsequent machine learning models. For future work, further feature engineering and selection could enhance the model's performance and predictions.

# Saving Cleaned Datasets

Finally, the cleaned datasets were saved as CSV files:

- Titanic_Train_Cleaned.csv
- Titanic_Test_Cleaned.csv

These files will be used in the next steps of predicting the survivors of the Titanic disaster.

# Data Visualizations

Several visualizations are created within the notebook using Matplotlib. I've added a screenshot of each to this repository:

- Survival Rates for Passengers with and without Missing Feature Values: Survival_CompleteInfo.png
- Regression Learning Curve Analysis: LC_Analysis_Regression.png
- Classification Learning Curve Analysis (CabinNumber_Group feature): LC_Analysis_Classification.png
- Prediction Score Comparision for Classification Models (CabinLetter_Cohort feature): Score_Analysis_CabinLetter_Cohort_Classification.png
- Survival Rates for Cabin Numbers: Survival_CabinNumber.png
- Survival Rates for Cabin Numbers (Grouped): Survival_CabinNumber_Grouped.png

# Contact

I appreciate your feedback and suggestions! Feel free to fork this project and edit as you please. If you'd like to pass along any suggestions, you can contact me at christianevans0226@gmail.com!

