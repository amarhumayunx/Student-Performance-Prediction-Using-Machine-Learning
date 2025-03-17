# 🎓 Student Performance Prediction System

This repository contains a machine learning project that predicts whether a student will pass or fail based on their academic, demographic, and social data. The project utilizes the **UCI Student Performance Dataset**, and the predictive model is built using a **Random Forest Classifier**.

## 📂 Dataset Information

- **Source**: [UCI Machine Learning Repository - Student Performance Data Set](https://archive.ics.uci.edu/ml/datasets/student+performance)
- The dataset includes information about student grades, demographics, social, and school-related features.
- Attributes include:
  - School, gender, age, address
  - Family background and education
  - Study time, failures, extracurricular activities
  - Alcohol consumption, health status, absences, etc.

## 🚀 Project Workflow

1. **Data Collection & Extraction**
   - Download the dataset zip file.
   - Extract CSV files (`student-mat.csv`).

2. **Data Preprocessing**
   - Convert categorical variables to numeric using **Label Encoding**.
   - Create a target label `pass` (1 if final grade `G3 >= 10`, else 0).
   - Drop the original `G1`, `G2`, and `G3` grade columns to avoid data leakage.
   - Scale features using **StandardScaler**.

3. **Handling Imbalanced Dataset**
   - Apply **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the target classes.

4. **Model Building**
   - Split the data into training and testing sets.
   - Perform **GridSearchCV** for hyperparameter tuning of **Random Forest Classifier**.
   - Evaluate the best model using cross-validation accuracy, test accuracy, classification report, and confusion matrix.

5. **Feature Importance**
   - Visualize the importance of features that contribute to the prediction.

6. **Predictions**
   - Predict outcomes for custom sample students to test the model.

## 🧰 Technologies and Libraries Used

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- imbalanced-learn (SMOTE)

## 📊 Model Evaluation

- **Accuracy**: Achieved through GridSearchCV optimization and cross-validation.
- **Classification Report**: Provides precision, recall, and F1-score.
- **Confusion Matrix**: Visualized for better understanding of model predictions.
- **Feature Importance**: Bar plot showing most influential features.

## 🏆 Results

- **Cross-Validation Accuracy (Train Set)**: 79.70% 
- **Final Model Accuracy (Test Set)**: 80.19%
