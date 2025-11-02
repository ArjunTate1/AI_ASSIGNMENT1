Heart Disease Prediction: Feature Engineering Pipeline 
This repository documents the comprehensive feature engineering pipeline applied to the Heart Disease Dataset (UCI Cleveland) to prepare the data for a classification model. The goal was to clean, scale, encode, and select the most impactful features to ensure high model performance and interpretability.


1. Dataset Overview
Dataset: Processed Cleveland Heart Disease Data (UCI ML Repository).

Problem Type: Classification (Predicting the presence of heart disease - target).

Initial Challenges: Missing values (represented by ?) and a mix of numerical, ordinal, and nominal categorical features.


2. Feature Engineering Steps Taken

Handling Missing Data: Missing values (represented by ? in the raw data) were replaced using Median Imputation for numerical features. This ensures the dataset is complete while minimizing distortion from potential outliers.Encoding Categorical Variables: Suitable categorical and ordinal features (like sex, cp, etc.) were converted using One-Hot Encoding (pd.get_dummies). This prevents the model from assigning false numerical relationships to categories.Feature Scaling: All resulting numerical features were subjected to Standardization (StandardScaler). This transforms the data to have a mean of 0 and a standard deviation of 1, ensuring all features contribute equally to the model.Dimensionality Reduction: Principal Component Analysis (PCA) was applied, typically set to retain a specific percentage of variance (like 95%) or a fixed number of components (e.g., $k=2$ as shown). This step decorrelates the features and reduces computational complexity.Feature Selection: SelectKBest with the $f\_{classif}$ score function was used to select the top 8 features. This process identifies and retains only the most statistically significant predictors of the target variable, which helps in reducing overfitting and improving model focus.


3.  Final Data State
The final dataset, X_new, represents the optimal input for the model:

It is complete (no NaNs).

All values are scaled and centered.

The dimensionality is reduced (optimized for simplicity).

It contains the 8 most predictive features for heart disease classification.

This rigorous preprocessing ensures the subsequent predictive model (e.g., Logistic Regression or SVM) operates with maximum efficiency and accuracy.