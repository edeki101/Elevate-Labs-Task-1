# Elevate Labs AI & ML Internship - Task 1

## Objective
This repository contains the completion of Task 1: Data Cleaning & Preprocessing. The goal is to clean and prepare raw data for machine learning models by handling missing values, encoding categorical variables, scaling features, and removing outliers.

## Dataset
Source:Titanic Dataset (`Titanic-Dataset.csv`)

## Tools Used
* Python
* Pandas & NumPy (Data manipulation)
* Matplotlib & Seaborn (Visualization)
* Scikit-learn (Feature scaling)

## Preprocessing Steps Completed
1. Data Inspection: Imported the dataset and checked for null values, data types, and basic statistics.
2. Handling Missing Values:
   * Dropped the `Cabin` column (77.10% missing).
   * Imputed the `Age` column (19.87% missing) using the median.
   * Imputed the `Embarked` column (0.22% missing) using the mode.
3. Categorical Encoding:
   * Dropped non-predictive unique identifiers (`PassengerId`, `Name`, `Ticket`).
   * Applied One-Hot Encoding to the `Sex` and `Embarked` columns, dropping the first category to prevent multicollinearity.
4. Feature Scaling: Applied `StandardScaler` to numerical features (`Age`, `Fare`) to center the data with a mean of 0 and a standard deviation of 1.
5. Outlier Removal:Visualized the `Fare` column using Seaborn boxplots and removed statistical outliers using the Interquartile Range (IQR) method.

## Files in this Repository
* `Task_1_Data_Cleaning.ipynb`: The Google Colab notebook containing the complete Python code.
* `Titanic-Dataset.csv`: The raw dataset used for this task.
* `README.md`: This documentation file.


---

## Interview Questions & Answers

1. What are the different types of missing data?
* Missing Completely at Random (MCAR):The missingness has no relationship with any other data.
* Missing at Random (MAR): The missingness is related to some other observed data, but not the missing value itself.
* Missing Not at Random (MNAR):The missingness is directly related to the value that is missing.

2. How do you handle categorical variables?
Categorical variables are handled using encoding techniques to convert text into numerical values that ML models can process, such as One-Hot Encoding or Label Encoding.

3. What is the difference between normalization and standardization?
Normalization scales values to a specific fixed range (usually 0 to 1). Standardization centers the data around a mean of 0 with a standard deviation of 1, which is more robust to outliers.

4. How do you detect outliers?
Outliers can be detected visually using boxplots or scatter plots, or statistically using the Interquartile Range (IQR) method or Z-scores.

5. Why is preprocessing important in ML?
Real-world data is messy. Preprocessing cleans the data, handles missing values, scales features, and removes noise, which prevents errors and reduces bias during model training.

6. What is one-hot encoding vs label encoding?
One-Hot Encoding creates new binary columns for each category (best for nominal, unranked data). Label Encoding assigns an integer to each category (best for ordinal, ranked data).

7. How do you handle data imbalance?
By using resampling techniques like oversampling the minority class, undersampling the majority class, or generating synthetic data using SMOTE.

8. Can preprocessing affect model accuracy?
Yes, preprocessing significantly impacts model accuracy. Models trained on unscaled data with missing values and severe outliers will generally perform poorly and make highly biased predictions.
