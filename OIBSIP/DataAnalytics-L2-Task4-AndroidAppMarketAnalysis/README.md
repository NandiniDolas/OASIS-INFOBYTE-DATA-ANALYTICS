# Android App Market Analysis

## Project Overview
This project analyzes Google Play Store applications and user reviews to understand app categories, ratings, installation counts, app sizes, pricing models, and review sentiment.

## Datasets
1. `googleplaystore.csv` — contains application information, including category, rating, reviews, size, installs, price, and last update.
2. `googleplaystore_user_reviews.csv` — contains user review text, sentiment labels, sentiment polarity, and subjectivity.

## Tools and Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Data Cleaning
- Examined missing values and duplicate records.
- Removed exact duplicate rows.
- Corrected a malformed app record.
- Handled missing descriptive information.
- Converted review counts and installation counts to numeric values.
- Converted app sizes into megabytes where possible.
- Converted prices to numeric values.
- Converted last-update values to datetime.
- Prepared a separate dataset containing reviews with available text and sentiment labels.

Missing app ratings and unavailable app sizes were retained as missing values rather than guessed.

## Exploratory Data Analysis
The project includes:
1. App distribution by category.
2. Distribution of app ratings.
3. Comparison of free and paid apps.
4. Analysis of the most-installed apps.
5. Distribution of app sizes.
6. Average ratings by category.
7. Distribution of positive, negative, and neutral user reviews.

## Key Findings
- FAMILY had the highest number of apps in the cleaned dataset.
- Most rated apps had ratings between 4.0 and 4.7.
- Free apps substantially outnumbered paid apps.
- Several popular Google services and communication apps had reported installation counts of one billion.
- Most apps were relatively small, with sizes concentrated below 10 MB.
- EVENTS had the highest average rating among the categories examined.
- Positive reviews were the most common sentiment in the available review data.

## Conclusion
The analysis provides an overview of app-market patterns, ratings, pricing models, app sizes, and user sentiment. These findings can help developers explore user preferences and identify opportunities for further analysis.

## Project Files
- `Android_App_Market_Analysis.ipynb` — analysis notebook
- `googleplaystore.csv` — apps dataset
- `googleplaystore_user_reviews.csv` — user reviews dataset
- `README.md` — project documentation
