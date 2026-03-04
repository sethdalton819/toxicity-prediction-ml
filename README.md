Toxicity Prediction using Random Forest
Project Overview

This project builds a machine learning classification model to predict whether a chemical compound is Toxic or NonToxic using ensemble learning (Random Forest).

Dataset Description

Total samples: 171

Total features: 1203

Target variable: Class

Binary classification problem

The dataset contains high-dimensional molecular descriptors used to predict toxicity.

Methodology
1. Data Preprocessing

Loaded dataset using pandas

Separated features (X) and target (y)

Encoded target variable using LabelEncoder

2. Feature Selection

Trained an initial Random Forest model

Ranked features based on importance

Selected top 50 most important features to reduce overfitting risk

3. Model Training

Split data into training (80%) and testing (20%)

Used RandomForestClassifier

Applied class_weight='balanced' to address class imbalance

Results

Confusion Matrix:

[[20  4]
 [ 9  2]]

Classification Summary:

Accuracy: 63%

NonToxic Recall: 0.83

Toxic Recall: 0.18

Interpretation

The model performs well in identifying NonToxic compounds but struggles with Toxic compounds due to:

Small dataset size

Moderate class imbalance

High dimensionality

Conclusion

Random Forest achieved moderate predictive performance. Future improvements could include:

Larger dataset

Boosting algorithms (e.g., Gradient Boosting)

Advanced resampling techniques
