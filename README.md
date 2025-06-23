# ⚓ ElevateLabs Task 1 – Titanic Dataset Cleaning & Preprocessing
This project demonstrates a structured approach to cleaning and preparing the Titanic dataset for machine learning applications. The primary aim is to make the raw passenger data usable for survival prediction models by addressing missing values, transforming features, scaling numerical values, and filtering out outliers.

## 🧾 About the Dataset
The `tested.csv` file contains records of Titanic passengers with features such as:
* `Pclass`: Travel class (1st, 2nd, 3rd)
* `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`, etc.
* `Survived`: Target column (1 if the passenger survived, 0 otherwise)
This dataset is adapted from the popular Titanic challenge on [Kaggle](https://www.kaggle.com/c/titanic).

## 🔍 Preprocessing Workflow
All preprocessing logic is implemented in the notebook `Titanic_survival.ipynb`, which walks through the following steps:
### 🧼 1. Data Inspection
* Used tools like `.info()`, `.describe()`, and visual checks to understand the data
* Null values highlighted using seaborn heatmaps and summary statistics
### 🩹 2. Dealing with Missing Values
* Replaced missing `Age` values with the median
* Imputed missing `Embarked` values using the most frequent category
* Dropped the `Cabin` feature due to excessive missing data
### 🔢 3. Encoding Categorical Data
* Transformed `Sex` into numerical values (0/1)
* Applied one-hot encoding to the `Embarked` column
### 📏 4. Feature Scaling
* Standardized `Age` and `Fare` using `StandardScaler` for normalization
### 🧾 5. Removing Outliers
* Visualized distributions using box plots
* Applied IQR filtering to drop outliers in continuous features
