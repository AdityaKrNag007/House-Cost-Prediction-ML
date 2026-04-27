# House Price Prediction (Advanced with Validation)

## Objective
Predict house prices using regression models and build a reliable evaluation pipeline.

## Dataset
Kaggle - House Prices: Advanced Regression Techniques

## Approach

### Data Processing
- Selected key numerical features (area, rooms, garage, quality)
- Handled missing values using median imputation

### Feature Engineering
- Created derived features:
  - HouseAge = CurrentYear - YearBuilt
  - TotalSF = 1stFlrSF + 2ndFlrSF
  - TotalRooms = TotalRooms + Bedrooms
- Added high-impact features:
  - OverallQual
  - GarageCars

### Data Splitting (Important)
- Train set → model training  
- Validation set → model tuning  
- Test set → final evaluation (kept untouched)

## Models Used
- Linear Regression
- Random Forest Regressor

## Results

| Model | MAE |
|------|------|
| Linear Regression | ~23162 |
| Random Forest | ~18816 |
| Validation MAE (RF) | ~19603 |
| Test MAE (RF) | ~19262 |

## Key Improvements
- Feature engineering significantly reduced error (~21k → ~18.8k)
- Added validation set to ensure unbiased model tuning
- Maintained separation of test data for reliable evaluation

## Key Learnings
- Feature quality impacts performance more than hyperparameter tuning
- Random Forest captures non-linear relationships effectively
- Proper evaluation (train/validation/test split) is critical for trustworthy models

## Conclusion
Built a robust regression pipeline with reliable evaluation, demonstrating strong generalization performance on unseen data.
