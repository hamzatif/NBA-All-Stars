# NBA All-Star Predictor

This project predicts NBA All-Star selections using historical player statistics and advanced machine learning models. The primary goal is to identify key player features that correlate with All-Star selections and use this data to predict future All-Stars effectively.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Description](#dataset-description)
3. [Data Preprocessing](#data-preprocessing)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis)
5. [Feature Engineering](#feature-engineering)
6. [Modeling](#modeling)
7. [Evaluation](#evaluation)
8. [Results](#results)

---

## Introduction

The NBA All-Star Predictor aims to:
- Analyze player performance metrics.
- Identify patterns associated with All-Star selections.
- Predict future All-Stars using machine learning models such as Logistic Regression, Decision Trees, Random Forest, XGBoost, and K-Nearest Neighbors.

---

## Dataset Description

The project utilizes two datasets:
- **Training Dataset (`ASG_train.csv`)**: Historical player statistics and All-Star selection labels.
- **Prediction Dataset (`ASG_to_predict.csv`)**: Current season statistics for prediction.

---

## Data Preprocessing

### Missing Data
Missing values were identified and addressed. Players with fewer than 7 games played were excluded.

### Outliers
Outliers (e.g., players with exceptionally rare All-Star appearances) were removed from the dataset based on historical inconsistencies.

### Normalization
Key performance metrics were adjusted using league-average pace to normalize the data.

### Feature Creation
- **`Play Pct.`**: Percentage of games played by a player compared to their team’s total games.
- **Adjusted Metrics**: Metrics such as `PTS`, `REB`, and `AST` were normalized by average pace.

---

## Exploratory Data Analysis

### Visualizations
- Class distribution of All-Star vs. Non-All-Star players.
- Histograms and boxplots of key features (e.g., `Adjusted PTS`, `Adjusted REB`).
- Correlation heatmaps to explore feature relationships.
- Violin plots to visualize feature distributions across All-Star selections.

---

## Feature Engineering

### Selected Features
Key features include:
- `Adjusted PTS`, `Adjusted REB`, `Adjusted AST`
- `DEFWS`, `USG%`, `PIE`
- `Prior ASG Appearances`, `Team Conference Rank`

---

## Modeling

### Models Used
1. **Logistic Regression**: Baseline classification model.
2. **Decision Tree Classifier**: Tree-based model for interpretable results.
3. **Random Forest**: Ensemble learning method.
4. **XGBoost**: Advanced boosting algorithm.
5. **K-Nearest Neighbors (KNN)**: Instance-based learning model.

### Oversampling
SMOTE was used to handle class imbalance for XGBoost and KNN.

### Hyperparameter Tuning
GridSearchCV was employed for hyperparameter optimization of Random Forest, XGBoost, and KNN models.

---

## Evaluation

### Metrics
- Accuracy
- Precision
- Recall
- F1 Score

### Confusion Matrices
Confusion matrices were plotted to evaluate true positives, false positives, true negatives, and false negatives.

---

## Results

1. **Random Forest**
   - Accuracy: 97.37%
   - Precision: 76%
   - Recall: 85.59%
   - F1 Score: 80.51%
2. **XGBoost**
   - Accuracy: 97.43%
   - Precision: 75.38%
   - Recall: 88.29%
   - F1 Score: 81.33%
3. **KNN**
   - Accuracy: 94.40%
   - Precision: 53.67%
   - Recall: 85.59%
   - F1 Score: 65.97%

Correct Predictions:
- Eastern Conference: 11 of 12 All-Stars.
- Western Conference: 10 of 13 All-Stars.
- Total: 21 of 25 All-Stars correctly predicted.

---

## Future Work
- Incorporate additional features (e.g., advanced defensive metrics).
- Test with alternative algorithms (e.g., Neural Networks).
- Enhance feature selection using automated methods.

---

For questions or contributions, feel free to reach out!

