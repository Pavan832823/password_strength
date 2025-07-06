# Password Strength Classifier

## Overview

This project implements a machine learning model to classify password strength into three categories: Weak, Medium, and Strong. The classifier uses XGBoost and evaluates passwords based on several features including length, character diversity, and special character usage.

## Features

- **Machine Learning Model**: Uses XGBoost classifier for password strength prediction
- **Feature Extraction**: Analyzes passwords based on:
  - Length
  - Number of uppercase letters
  - Number of lowercase letters
  - Number of digits
  - Number of special characters
- **Performance Metrics**: Reports model accuracy on test data
- **Interactive Testing**: Allows users to input passwords and get immediate strength evaluations

## Requirements

- Python 3.8+
- Required packages:
  - pandas
  - numpy
  - scikit-learn
  - xgboost

Install dependencies with:
```bash
pip install pandas numpy scikit-learn xgboost
```

## Usage

1. Prepare your password dataset in a CSV file named `data.csv` with columns:
   - `password`: The password strings
   - `strength`: Strength labels (0=Weak, 1=Medium, 2=Strong)

2. Run the Jupyter notebook:
```bash
jupyter notebook password_strength.ipynb
```

3. The notebook will:
   - Load and preprocess the data
   - Train the XGBoost model
   - Report model accuracy
   - Prompt you to test passwords interactively

## Example Output

```
Model Accuracy: 1.00
Enter Password: MySecurePass123!
Password: MySecurePass123! | Strength: Strong
```

## Implementation Details

- **Data Preparation**: The dataset is cleaned and labels are mapped to numerical values
- **Feature Engineering**: Extracts 5 key features from each password
- **Model Training**: Uses XGBoost with 100 estimators
- **Evaluation**: Reports accuracy on a held-out test set (20% of data)

## Future Improvements

- Add more sophisticated feature extraction (common password patterns, entropy calculation)
- Implement a web interface for easier testing
- Add password generation suggestions
- Include more comprehensive security metrics

