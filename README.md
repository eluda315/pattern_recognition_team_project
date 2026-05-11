# Income Prediction Project

## Overview
Binary classification project to predict whether annual income is greater than `$50K`.

- Target: `income`
- Metric: `(F1 Score + AUC) / 2`

## Dataset
- `train.csv`: 39,073 rows × 15 columns
- `test.csv`: 9,769 rows × 14 columns
- Test set does not include `income`.

## Current Progress

### Preprocessing
- Loaded train/test datasets
- Checked column types and missing values
- Found missing values in categorical columns:
  - `workclass`
  - `occupation`
  - `native_country`
- Filled categorical missing values using train-set mode as baseline
- Converted target label:
  - `<=50K` → 0
  - `>50K` → 1
- Applied one-hot encoding to categorical features

## Output
Current preprocessing creates:

- `X_train`: `(39073, 105)`
- `X_test`: `(9769, 105)`
- `y_train`: encoded target labels
- `test_id`: id column for submission

## Next Steps
- Confirm preprocessing strategy with team
- Train baseline models
- Evaluate using F1 and AUC
- Generate `prediction.csv`