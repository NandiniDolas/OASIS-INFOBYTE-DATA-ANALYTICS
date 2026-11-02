# Wine Quality Prediction

## Project Overview
This project focuses on analyzing red wine chemical properties and predicting wine quality categories using machine learning classification algorithms. It was completed as part of the Oasis Infobyte Data Analytics Internship.

## Dataset
The project uses the Red Wine Quality dataset (`winequality-red.csv`).

The dataset contains chemical measurements of red wine samples and a quality score for each sample.

## Objectives
- Explore and understand the dataset.
- Analyze the distribution of wine quality scores.
- Visualize chemical feature distributions and correlations.
- Handle class imbalance by grouping quality scores into categories.
- Train and evaluate multiple machine learning classification models.
- Identify important chemical features and compare model performance.

## Tools and Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow
1. Load and inspect the dataset.
2. Check missing values and duplicate records.
3. Analyze wine quality score distribution.
4. Visualize chemical feature distributions.
5. Create a correlation heatmap.
6. Group quality scores into three categories:
   - Low: Quality score ≤ 5
   - Medium: Quality score = 6
   - High: Quality score ≥ 7
7. Split the dataset into training and testing sets using stratified sampling.
8. Train three classification models:
   - Random Forest Classifier
   - SGD Classifier
   - Support Vector Classifier (SVC)
9. Evaluate models using accuracy, precision, recall, F1-score, classification reports, and confusion matrices.
10. Visualize Random Forest feature importance.
11. Compare model performance and identify the most suitable model.

## Project Files
- `Task_2_Wine_Quality_Prediction.ipynb` — Jupyter Notebook containing the analysis, visualizations, model training, and evaluation.
- `winequality-red.csv` — Dataset used for the project.
- `README.md` — Project documentation.

## Results
Three machine learning classification models were trained and evaluated. Their performance was compared using accuracy, precision, recall, and weighted F1-score.

The model with the highest weighted F1-score is selected as the best-performing model for this project. Refer to the notebook's model comparison table for the actual results.

## Conclusion
This project demonstrates how exploratory data analysis and machine learning can be applied to predict wine quality categories using chemical properties. It also highlights the importance of class distribution, model evaluation, and feature importance in a classification task.

## Author
Completed as part of the Oasis Infobyte Data Analytics Internship.
