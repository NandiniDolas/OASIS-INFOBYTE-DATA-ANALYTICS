# Credit Card Fraud Detection

## Project Overview
This project uses machine learning to identify potentially fraudulent credit card transactions. It explores transaction data, addresses class imbalance, trains classification models, and compares their performance.

## Dataset
- **File:** `creditcard.csv`
- **Rows after duplicate removal:** 283,726
- **Features used for modeling:** 30
- **Target:** `Class` (0 = Normal, 1 = Fraud)
- **Fraud cases after duplicate removal:** 473

The dataset contains anonymized features V1–V28, along with transaction time and amount.

## Project Steps
1. Loaded and inspected the dataset.
2. Checked missing values and duplicate records.
3. Removed exact duplicate rows.
4. Performed exploratory data analysis using visualizations.
5. Examined the class imbalance.
6. Split the data into training and testing sets using stratification.
7. Scaled the Time and Amount features for Logistic Regression.
8. Trained Logistic Regression and Random Forest models.
9. Evaluated the models using accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrices.
10. Compared ROC curves and examined Random Forest feature importance.

## Model Results

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 0.9752 | 0.9994 |
| Precision | 0.0562 | 0.8861 |
| Recall | 0.8737 | 0.7368 |
| F1-Score | 0.1057 | 0.8046 |
| ROC-AUC | 0.9658 | 0.9708 |

## Key Findings
- The dataset is highly imbalanced, so accuracy alone is insufficient.
- Logistic Regression detected 83 of 95 fraud cases in the test set but generated 1,393 false positives.
- Random Forest detected 70 of 95 fraud cases and generated 9 false positives.
- Random Forest achieved a higher precision, F1-score, and ROC-AUC.
- V14, V10, V12, V4, and V17 were among the most important features in the Random Forest model.

## Conclusion
Random Forest provided a better balance between precision and recall at the default classification threshold, while Logistic Regression detected more fraud cases. The preferred model depends on the relative cost of missed fraud and false alarms.

## Limitations and Future Improvements
- Tune classification thresholds to balance fraud detection and false positives.
- Test models on additional data and realistic transaction streams.
- Monitor changing fraud patterns and retrain models when necessary.
- Evaluate processing speed and reliability before production deployment.

## Tools and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Disclaimer
This project is an educational prototype. It is not a production-ready fraud detection system.
