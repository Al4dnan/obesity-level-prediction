# Obesity Level Prediction Using Machine Learning

### Classifying Obesity Levels from Eating Habits and Physical Condition

## 📌 Project Overview

This project focuses on predicting obesity levels based on individuals' eating habits, lifestyle patterns, demographic information, and physical condition using Machine Learning algorithms.

The main objective is to develop and evaluate supervised classification models that can classify individuals into seven different obesity categories using the UCI Obesity Dataset.

The project also investigates how including Height and Weight affects prediction performance and demonstrates the problem of **Target Leakage** in Machine Learning.

## 👨‍💻 Author

**Al Adnan**

- University: Lovely Professional University
- Programme: B.Tech - Computer Science and Engineering
- Registration Number: 12402657
- Section: K24P24CQ
- Project Supervisor: Manpreet Kaur

## 🎯 Project Objectives

- Analyze obesity-related data using Exploratory Data Analysis (EDA).
- Clean and preprocess the dataset.
- Identify patterns and relationships between lifestyle factors and obesity levels.
- Implement multiple Machine Learning classification algorithms.
- Evaluate and compare model performance.
- Identify important features influencing predictions.
- Demonstrate the effect of target leakage using Height and Weight.

## 📊 Dataset Information

**Dataset Name:** Estimation of Obesity Levels Based on Eating Habits and Physical Condition

**Source:** UCI Machine Learning Repository

**Dataset Link:** https://archive.ics.uci.edu/dataset/544

| Dataset Details | Information |
|---|---|
| Original Records | 2,111 |
| Features | 17 |
| Records after cleaning | 2,087 |
| Duplicate Records Removed | 24 |
| Target Variable | NObeyesdad |
| Classification Classes | 7 |
| Missing Values | 0 |

The dataset contains information about individuals from Mexico, Peru, and Colombia.

Approximately 77% of the records were synthetically generated using SMOTE, while 23% were collected directly from users. This is an important limitation when interpreting model performance.

### Obesity Classification Categories

1. Insufficient Weight
2. Normal Weight
3. Overweight Level I
4. Overweight Level II
5. Obesity Type I
6. Obesity Type II
7. Obesity Type III

## 🔍 Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to understand the dataset, identify patterns, and explore relationships between different variables.

The analysis included:

- Dataset structure and information.
- Duplicate and missing-value analysis.
- Obesity level distribution.
- Age distribution and analysis.
- Categorical variable distribution.
- Correlation matrix.
- BMI analysis by obesity category.
- Gender distribution across obesity levels.

## ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

- Removal of duplicate records.
- Missing-value checks.
- Feature selection.
- Label encoding of the target variable.
- One-hot encoding of categorical features.
- Stratified train-test splitting.
- Feature scaling using StandardScaler.

The cleaned dataset was divided into 80% training data and 20% testing data.

## 🤖 Machine Learning Algorithms

Four supervised Machine Learning classification algorithms were implemented and evaluated.

### 1. Logistic Regression
A classification algorithm used to predict obesity categories based on lifestyle and demographic features.

### 2. Decision Tree Classifier
A tree-based algorithm that makes predictions through a sequence of decision rules.

### 3. Random Forest Classifier
An ensemble learning algorithm that combines multiple decision trees to improve classification performance.

### 4. K-Nearest Neighbors (KNN)
A distance-based classification algorithm that predicts categories using the nearest training samples.

## 📈 Model Performance Comparison

The models were evaluated using the test dataset containing 418 records.

| Machine Learning Model | Accuracy | Macro F1 Score |
|---|---:|---:|
| Logistic Regression | 63.16% | 59.81% |
| Decision Tree | 69.14% | 68.79% |
| Random Forest | 83.97% | 83.68% |
| K-Nearest Neighbors | 76.08% | 75.00% |

### 🏆 Best Performing Model

**Random Forest Classifier**

- Accuracy: 83.97%
- Macro Precision: 84.00%
- Macro Recall: 83.66%
- Macro F1 Score: 83.68%

Random Forest achieved the best overall performance in the lifestyle-only experiment.

## 📉 Model Evaluation

The following evaluation techniques were used:

- Accuracy Score
- Precision
- Recall
- Macro F1 Score
- Classification Report
- Confusion Matrix
- Feature Importance Analysis

## 🎯 Feature Importance

Random Forest feature importance was used to identify influential input features.

The most important features included:

1. Age
2. Frequency of Vegetable Consumption (FCVC)
3. Number of Main Meals (NCP)
4. Physical Activity Frequency (FAF)
5. Time Using Technology Devices (TUE)
6. Daily Water Consumption (CH2O)

These values represent the features used by the model and should not be interpreted as proof of causal relationships.

## ⚠️ Target Leakage Experiment

An additional experiment was conducted by including Height and Weight as input features.

Since the obesity classification labels are derived from BMI, which is calculated using Height and Weight, including these variables can introduce target leakage.

### Accuracy Comparison

| Model | Lifestyle Only | With Height & Weight |
|---|---:|---:|
| Logistic Regression | 63.16% | 89.23% |
| Decision Tree | 69.14% | 93.54% |
| Random Forest | 83.97% | 93.06% |
| KNN | 76.08% | 80.86% |

The improved accuracy in this experiment does not necessarily indicate better lifestyle-based prediction. It mainly reflects the models learning information directly related to how the target labels were created.

Therefore, the lifestyle-only experiment is treated as the main result.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook / Python Environment

## 📁 Project Structure

```text
obesity-level-prediction/
│
├── obesity_level_prediction.py
├── ObesityDataSet.csv
├── README.md
├── requirements.txt
├── Project_Report.pdf
│
└── figures/
    ├── distribution.png
    ├── correlation_heatmap.png
    ├── model_comparison.png
    ├── confusion_matrices.png
    └── feature_importance.png
```

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/Al4dnan/obesity-level-prediction.git
```

### Step 2: Navigate to the Project Folder

```bash
cd obesity-level-prediction
```

### Step 3: Install Required Libraries

```bash
pip install -r requirements.txt
```

### Step 4: Run the Python Script

```bash
python obesity_level_prediction.py
```

Make sure the dataset file `ObesityDataSet.csv` is available in the project directory.

## 🔮 Future Scope

The project can be improved further through:

- Implementation of advanced algorithms such as XGBoost and LightGBM.
- Hyperparameter tuning and cross-validation.
- Evaluation using additional real-world datasets.
- Improved class-specific prediction performance.
- Explainable AI techniques such as SHAP.
- Development of a web-based obesity prediction application.

## 📌 Conclusion

This project demonstrates the application of Machine Learning techniques for classifying obesity levels using eating habits and physical-condition variables.

Among the four evaluated algorithms, Random Forest achieved the best performance with 83.97% accuracy and an 83.68% macro F1 score in the lifestyle-only experiment.

The target leakage experiment also highlighted the importance of selecting appropriate input features and understanding how target variables are generated.

Overall, this project provides practical experience in data preprocessing, exploratory data analysis, supervised learning, model evaluation, and feature importance analysis.

## 🙏 Acknowledgement

I would like to express my sincere gratitude to my project supervisor, **Manpreet Kaur**, and the faculty members of Lovely Professional University for their guidance and academic support.

I also acknowledge the UCI Machine Learning Repository for providing the dataset used in this project.

## ⚠️ Disclaimer

This project is developed for academic, educational, and research purposes only. It is not a clinically validated medical diagnostic or screening tool.

## 📚 References

1. UCI Machine Learning Repository – Estimation of Obesity Levels Based on Eating Habits and Physical Condition.
2. Pandas Documentation – https://pandas.pydata.org/docs/
3. NumPy Documentation – https://numpy.org/doc/
4. Scikit-learn Documentation – https://scikit-learn.org/stable/
5. Matplotlib Documentation – https://matplotlib.org/
