# Titanic — EDA & Machine Learning
 
A two-notebook project exploring the Titanic dataset with full exploratory data analysis and a comparison of 8 classification models.
 
---
 
## Notebooks
 
### 1. `Titanic_EDA.ipynb` — Exploratory Data Analysis
 
Analyzes the dataset to uncover survival patterns before any modeling.
 
| Task | What's covered |
|---|---|
| Data Inspection | Shape, types, missing values, descriptive stats |
| Univariate Analysis | Survival rate, passenger class distribution |
| Bivariate Analysis | Survival by Sex, Pclass, Age, Embarked port |
| Conclusions | Top predictors identified: **Gender, Class, Age** |
 
**Key Findings:**
- **Females** had a ~74% survival rate vs ~19% for males
- **1st class** passengers survived at ~63% vs ~24% for 3rd class
- **Children (0–10)** survived more; **elderly (65+)** were least likely to survive
---
 
### 2. `TitanicDataset_Train.ipynb` — Model Training & Comparison
 
Trains 8 classifiers after preprocessing and compares their accuracy.
 
**Preprocessing steps:** drop irrelevant columns → fill missing values → engineer `FamilySize` / `IsAlone` features → encode categoricals → scale features
 
#### Model Accuracy (Test Set)
 
| Rank | Model | Accuracy |
|---|---|---|
| 🥇 1 | Random Forest | 83.24% |
| 🥈 2 | Perceptron | 81.01% |
| 🥈 2 | SVC | 81.01% |
| 4 | KNN | 80.45% |
| 5 | Decision Tree | 79.89% |
| 5 | Logistic Regression | 79.89% |
| 7 | Naive Bayes | 78.77% |
| 8 | SGD | 76.54% |
 
> **Best model: Random Forest** with **83.24%** accuracy.
 
---
 
## Requirements
 
```
pandas
scikit-learn
matplotlib
seaborn
joblib
```
 
```bash
pip install pandas scikit-learn matplotlib seaborn joblib
```
 
---
 
## Dataset
 
[Titanic CSV](https://raw.githubusercontent.com/datasciencedojo/datasets/refs/heads/master/titanic.csv) via DataScienceDojo — loaded directly from URL, no local file needed.
 
