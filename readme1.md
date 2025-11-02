Wine Quality Dataset

1. Data Cleaning (Imputation Check):
    Technique: Confirmed the absence of missing values, making the SimpleImputer step a check rather than an action.

    Impact: Ensures data integrity; the dataset is inherently clean and ready for numerical processing.

2. Categorical Encoding:
    Technique: Not Applicable (N/A) as all 11 features are purely numerical (physicochemical properties).

    Impact: No change to the feature space.

3. Feature Scaling (Standardization):
    Technique: Applied StandardScaler to all features, transforming them to have a mean of 0 and standard deviation of approx 1.

    Impact: Equalizes feature influence. Features measured on disparate scales (e.g., 'alcohol' vs. 'fixed acidity') now contribute equally to model calculations, which is vital for distance-based and gradient descent algorithms.
4. Dimensionality Reduction (PCA):
    Technique: Used Principal Component Analysis (PCA) to create a smaller set of uncorrelated features (principal components).
    
    Impact: Reduces redundancy and dimensionality (e.g., from 11 features down to  7-8 components to retain most variance), improving model efficiency and mitigating multicollinearity.4

5. Feature Selection (Correlation Analysis/SelectKBest):
    Technique: Analyzed feature correlation with the target (quality) or used a statistical test like SelectKBest.

    Impact: Identifies and retains the most predictive original features (like 'alcohol' and 'volatile acidity'), offering a more interpretable and potentially simpler model input.
 
