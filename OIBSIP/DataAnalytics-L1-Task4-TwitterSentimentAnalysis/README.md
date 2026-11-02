# Task 4: Twitter Sentiment Analysis

## Project Overview
This project uses Natural Language Processing (NLP) and machine learning to classify tweets into four sentiment categories: Positive, Negative, Neutral, and Irrelevant.

## Objective
To analyze Twitter text and build machine-learning models that identify the sentiment expressed in each tweet.

## Dataset
The project uses the Twitter Entity Sentiment Analysis dataset, consisting of:
- Training dataset: 74,682 rows
- Validation dataset: 1,000 rows
- Features: ID, Topic, Sentiment, and Tweet
- Sentiment categories: Positive, Negative, Neutral, and Irrelevant

## Tools and Technologies
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- NLTK
- Scikit-learn
- Jupyter Notebook

## Project Workflow
1. Loaded and inspected the training and validation datasets.
2. Examined the distribution of sentiment categories.
3. Cleaned tweet text by converting it to lowercase and removing URLs, mentions, punctuation, and extra spaces.
4. Removed common stopwords while preserving important negation words such as "not" and "no".
5. Converted text into numerical features using TF-IDF.
6. Trained and evaluated two classification models.
7. Created a sentiment distribution chart, confusion matrices, and word-frequency charts.
8. Examined five misclassified tweets and discussed possible reasons for errors.

## Models and Results

| Model | Validation Accuracy |
|---|---:|
| Multinomial Naive Bayes | 75.9% |
| Logistic Regression | 86.5% |

Logistic Regression achieved higher validation accuracy in this experiment.

## Visualizations
- Sentiment distribution
- Confusion matrices for both models
- Most frequent words for each sentiment category

**Note:** Word-frequency charts were used instead of WordClouds because the WordCloud package could not be installed.

## Error Analysis
Some tweets were misclassified because of slang, sarcasm, spelling variations, ambiguous expressions, and limited context. These challenges can affect the accuracy of sentiment classification.

## Conclusion
This project demonstrates how NLP and machine learning can be used to classify social media sentiment. Logistic Regression performed better than Multinomial Naive Bayes on the validation dataset.

Sentiment analysis can help organizations understand customer feedback, monitor public opinion, and identify common reactions to products and services.

## Files
- `Task_4_Twitter_Sentiment_Analysis.ipynb` — notebook containing the analysis and models
- `twitter_training.csv` — training dataset
- `twitter_validation.csv` — validation dataset

## Author
Nandini Dolas
