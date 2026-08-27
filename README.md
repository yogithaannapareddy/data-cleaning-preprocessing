# Data Cleaning & Preprocessing

## 📌 Project Overview

This project focuses on cleaning and preprocessing the **Titanic dataset** for Machine Learning.

The main objective is to understand how raw data can be cleaned, transformed, and prepared before using it for Machine Learning models.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## 📂 Project Structure

```text
data-cleaning-preprocessing/
│
├── dataset/
│   ├── titanic.csv
│   └── titanic_cleaned.csv
│
├── notebooks/
│   └── data_preprocessing.ipynb
│
├── images/
│   ├── age_before.png
│   └── age_after.png
│
├── README.md
└── requirements.txt
```

## 🔍 Data Preprocessing Steps

### 1. Data Exploration

The dataset was explored using:

* `head()`
* `shape`
* `info()`
* `describe()`
* `dtypes`

Missing values were also identified using `isnull().sum()`.

### 2. Handling Missing Values

Missing values were handled using appropriate imputation techniques:

* **Age** → Median
* **Embarked** → Mode
* **Cabin** → Removed because it contained many missing values

### 3. Removing Unnecessary Columns

The following columns were removed:

* PassengerId
* Name
* Ticket

These columns were not required for this preprocessing task.

### 4. Categorical Encoding

Categorical features were converted into numerical values using **One-Hot Encoding**.

The following columns were encoded:

* Sex
* Embarked

### 5. Outlier Detection

Outliers were visualized using **boxplots**.

The following numerical features were analyzed:

* Age
* Fare

The **Interquartile Range (IQR)** method was used to detect and remove outliers.

### 6. Feature Scaling

Numerical features were standardized using **StandardScaler**.

The following features were scaled:

* Age
* Fare
* SibSp
* Parch

After standardization, the features have approximately a mean of 0 and a standard deviation of 1.

### 7. Saving the Cleaned Dataset

After preprocessing, the cleaned dataset was saved as:

```text
dataset/titanic_cleaned.csv
```

## 📊 Visualizations

Boxplots were created to visualize the data before and after outlier removal.

* `age_before.png` → Age distribution before outlier removal
* `age_after.png` → Age distribution after outlier removal

## 🎯 Key Learnings

Through this project, I learned:

* How to explore a dataset using Pandas.
* How to identify and handle missing values.
* How to encode categorical variables.
* How to detect and remove outliers using IQR.
* How to standardize numerical features.
* Why data preprocessing is important in Machine Learning.

## 💡 Interview Questions Covered

1. What are the different types of missing data?
2. How do you handle categorical variables?
3. What is the difference between normalization and standardization?
4. How do you detect outliers?
5. Why is preprocessing important in Machine Learning?
6. What is One-Hot Encoding vs Label Encoding?
7. How do you handle data imbalance?
8. Can preprocessing affect model accuracy?

## ✅ Conclusion

Data preprocessing is an important step in Machine Learning. Properly cleaned and transformed data can help Machine Learning algorithms work more effectively and produce reliable results.
