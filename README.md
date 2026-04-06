# 🍄 Mushroom Classification Project
## 📌 Overview

This project focuses on building a machine learning model to classify mushrooms as Edible (e) or Poisonous (p) based on their physical characteristics.

The dataset contains various categorical features such as cap shape, odor, gill color, and habitat. The goal is to leverage these features to achieve high classification accuracy.

## 🎯 Objective
Predict whether a mushroom is edible or poisonous
Build a robust ML pipeline
Avoid data leakage
Optimize model performance using hyperparameter tuning

## 📊 Dataset Description
Total Samples (Train): 7000
Test Samples: 1124
Features: 24
Target: class (e = edible, p = poisonous)
Feature Types:
🟣 Categorical: Majority (odor, gill-color, habitat, etc.)
🔵 Numerical: number_of_bruises

## 🧹 Data Preprocessing
🔹 Missing Values
Categorical → filled with "missing"
Numerical → filled with median
🔹 Duplicates
No duplicate rows found
🔹 Outliers
Outlier handling skipped as features are mostly categorical

## ⚙️ Feature Engineering & Pipeline
Used One-Hot Encoding for categorical features
Built a ColumnTransformer pipeline to:
Ensure consistent preprocessing
Prevent data leakage
Improve reproducibility

## 📈 Exploratory Data Analysis

Key insights:

Dataset is balanced → accuracy is reliable
Odor is highly predictive (almost deterministic)
Gill color strongly correlates with class
Habitat influences distribution of edible vs poisonous mushrooms

## 🤖 Models Used
Decision Tree
Random Forest
Extra Trees
HistGradientBoosting
XGBoost
LightGBM
CatBoost

##🧪 Model Performance

All models achieved:

✅ Accuracy: 1.0 (Validation)
✅ AUC: 1.0

👉 Indicates dataset is highly separable

## 🔧 Hyperparameter Tuning

Performed using RandomizedSearchCV on:

Random Forest
HistGradientBoosting
XGBoost

Result:

No significant improvement (already optimal performance)

## 🏆 Final Model Selection

Selected Random Forest due to:

Stability
Simplicity
Strong generalization
No dependency overhead

## 📤 Submission
Model trained on full dataset
Predictions generated for test data
Labels converted:
0 → e
1 → p

## 📁 Submission Format:
ID, class
1, e
2, p
...

## 📊 Final Results
Leaderboard Score: 0.99288
Rank: Top 100

## 🧠 Key Learnings
Proper preprocessing is more important than complex models
Categorical feature handling is critical
Pipelines help prevent data leakage
Some datasets are nearly perfectly separable

## 🚀 Future Improvements
Use CatBoost with native categorical handling
Feature interaction engineering (e.g., odor + gill-color)
Advanced ensembling techniques

## 🛠️ Tech Stack
Python
Pandas, NumPy
Scikit-learn
XGBoost, LightGBM, CatBoost
Matplotlib

## 📌 How to Run
# Clone repo
git clone <your-repo-link>

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook

## 👤 Author

Sarowar Ahmed

⭐ If you found this useful, give it a star!
