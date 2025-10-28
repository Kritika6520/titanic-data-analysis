# Titanic Data Analysis & Feature Engineering
This project focuses on performing Exploratory Data Analysis (EDA) and Feature Engineering (FE) on the Titanic dataset.
The goal was to understand the data, clean it, handle missing values, and create new meaningful features that could later help improve survival prediction models.

# Dataset
The dataset used is the Titanic dataset, which provides details about passengers such as their age, class, gender, and survival status.
Loaded using:
import seaborn as sns
data = sns.load_dataset("titanic")

# Data Cleaning Steps
Handled missing values in:
age → filled with median
deck, embarked, embark_town → filled with mode
Dropped irrelevant columns: alive, class, who, adult_male
Removed unnecessary duplicates (if any)

# Feature Engineering
New features were created to improve potential model performance:
family_size → sibsp + parch + 1
is_alone → 1 if passenger has no family, else 0
age_bin → Binned age into categories: child, teen, young_adult, adult, senior
fare_bin → Divided fare into 4 quartiles: low, medium, high, very_high
One-hot encoding → Applied to categorical columns
Feature Scaling → Used StandardScaler for numerical features like age, fare, etc.

# Insights from EDA
Younger passengers and females had higher survival rates.
Passengers with smaller families had better chances of survival.
Higher ticket prices often correlated with better survival rates.

# Output
Final cleaned dataset was saved as:
titanic_cleaned.csv
This file is ready for future model training and analysis.

# Tools & Libraries
Python
Pandas
NumPy
Seaborn
Matplotlib
Scikit-learn

# Future Work
Train ML models (e.g., Logistic Regression, Random Forest) for survival prediction.
Perform hyperparameter tuning and model evaluation.

# Author
Kritika Prabhu Penta
BCA Student | Aspiring Python & ML Developer
Mumbai, India
