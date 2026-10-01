# Elevate Labs AI & ML Internship - Task 1

## Objective
This repository contains the completion of Task 1: Data Cleaning & Preprocessing. The goal is to clean and prepare raw data for machine learning models by handling missing values, encoding categorical variables, scaling features, and removing outliers.

## Dataset
* **Source:** Titanic Dataset (`Titanic-Dataset.csv`)

## Tools Used
* Python
* Pandas & NumPy (Data manipulation)
* Matplotlib & Seaborn (Visualization)
* Scikit-learn (Feature scaling)

## Preprocessing Steps Completed
1. **Data Inspection:** Imported the dataset and checked for null values, data types, and basic statistics.
2. **Handling Missing Values:** 
   * Dropped the `Cabin` column (77.10% missing).
   * Imputed the `Age` column (19.87% missing) using the median.
   * Imputed the `Embarked` column (0.22% missing) using the mode.
3. **Categorical Encoding:** 
   * Dropped non-predictive unique identifiers (`PassengerId`, `Name`, `Ticket`).
   * Applied One-Hot Encoding to the `Sex` and `Embarked` columns, dropping the first category to prevent multicollinearity.
4. **Feature Scaling:** Applied `StandardScaler` to numerical features (`Age`, `Fare`) to center the data with a mean of 0 and a standard deviation of 1.
5. **Outlier Removal:** Visualized the `Fare` column using Seaborn boxplots and removed statistical outliers using the Interquartile Range (IQR) method.

## Files in this Repository
* `Task_1_Data_Cleaning.ipynb`: The Google Colab notebook containing the complete Python code.
* `Titanic-Dataset.csv`: The raw dataset used for this task.
* `README.md`: This documentation file.
