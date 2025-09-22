# Titanic Dataset: Data Cleaning and Preprocessing

This project focuses on the essential data cleaning and preprocessing steps required to prepare the Titanic dataset for machine learning analysis. The goal is to transform the raw data into a clean, structured, and numerical format suitable for modeling.

---

## 🛠️ Tools and Libraries Used
* **Python**
* **Pandas** for data manipulation and analysis.
* **NumPy** for numerical operations.
* **Matplotlib & Seaborn** for data visualization.
* **Scikit-learn** for feature scaling.

---

## 🧹 Preprocessing Steps

The following steps were performed to clean and prepare the data:

1.  **Data Loading & Exploration:** The `Titanic-Dataset.csv` was loaded into a pandas DataFrame. Initial exploration was done using `.info()`, `.head()`, and `.isnull().sum()` to understand the data's structure, identify data types, and locate missing values.

2.  **Handling Missing Data:**
    * **Age:** Missing values were filled with the **median** age to avoid the influence of outliers.
    * **Embarked:** The two missing values were filled with the **mode** (the most common port of embarkation).
    * **Cabin:** This column was **dropped** due to having a large number of missing values.

3.  **Feature Engineering & Encoding:**
    * Irrelevant columns (`PassengerId`, `Name`, `Ticket`) were dropped.
    * Categorical features (`Sex`, `Embarked`) were converted into numerical format using **one-hot encoding**.

4.  **Numerical Feature Scaling:**
    * The `Age` and `Fare` columns were standardized using **StandardScaler** from scikit-learn. This scales the features to have a mean of 0 and a standard deviation of 1.

5.  **Outlier Detection and Removal:**
    * **Box plots** were used to visualize outliers in the `Age` and `Fare` columns.
    * Outliers were removed using the **Interquartile Range (IQR)** method, resulting in a cleaner dataset for model training.

---

## ✅ Final Output

The final output is a fully preprocessed and cleaned DataFrame, ready to be used for training a machine learning model to predict passenger survival on the Titanic.
