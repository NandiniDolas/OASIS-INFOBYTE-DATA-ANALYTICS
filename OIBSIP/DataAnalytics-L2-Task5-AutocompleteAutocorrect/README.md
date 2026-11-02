# Autocomplete and Autocorrect Data Analytics

## Project Overview
This project explores autocomplete and autocorrect techniques using a large email text dataset. It uses natural language processing techniques, n-gram frequency analysis, and edit-distance algorithms to predict the next word and suggest spelling corrections.

## Objectives
- Preprocess email text for analysis.
- Build an autocomplete model using bigrams and trigrams.
- Test autocomplete predictions on 10 prefixes.
- Implement autocorrect using edit distance.
- Test autocorrect on 20 misspelled words.
- Compare Levenshtein and Damerau–Levenshtein algorithms.
- Evaluate model performance and visualize results.

## Dataset
The project uses a Kaggle email dataset containing 517,401 rows and two columns:
- `file`: email file path.
- `message`: email content.

A subset of 50,000 rows was selected for analysis. After removing empty messages and messages with fewer than two tokens, 49,764 messages remained.

The dataset is not included in this repository.

## Tools and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- NLTK
- Textdistance
- Scikit-learn
- Jupyter Notebook

## Methodology

### 1. Text Preprocessing
- Removed email headers.
- Converted text to lowercase.
- Removed URLs, punctuation, and digits.
- Normalized whitespace.
- Tokenized messages into words.

### 2. Autocomplete
Bigram and trigram frequencies were used to predict the next word based on the preceding one or two words. The model returned the three most frequent predictions.

### 3. Autocorrect
The model compared misspelled words with vocabulary words using:
- Levenshtein distance
- Damerau–Levenshtein distance

Candidate words were ranked by edit distance and word frequency.

### 4. Evaluation
Autocomplete was evaluated on 10 prefixes, while autocorrect was tested on 20 misspelled words. Accuracy, precision, recall, F1-score, and visualizations were used to examine model performance.

## Results

### Autocomplete
- Top-1 accuracy: 100% on the selected 10-prefix consistency check.
- Top-3 accuracy: 100% on the same test.

**Note:** Expected next words were taken from earlier model predictions. These scores are not an independent estimate of general performance.

### Autocorrect

| Algorithm | Top-1 Accuracy | Top-3 Accuracy |
|---|---:|---:|
| Levenshtein | 55% | 80% |
| Damerau–Levenshtein | 90% | 100% |

Damerau–Levenshtein performed better on the selected 20-word test set.

For the top-1 exact-match evaluation, precision, recall, and F1-score were 55% for Levenshtein and 90% for Damerau–Levenshtein.

## Visualizations
The notebook includes:
- Bar chart of the top 20 most frequent words.
- Confusion matrix for autocorrect predictions.
- Model evaluation results table.

## Limitations
- The models were built using a subset of the full dataset.
- Email-specific words and abbreviations can affect predictions.
- N-gram autocomplete does not understand the full meaning of a sentence.
- Edit-distance methods can suggest incorrect but similarly spelled words.
- The test sets are small.
- Autocomplete needs evaluation on an independent test set.
- Searching a large vocabulary can be computationally expensive.

## Conclusion
This project demonstrates how text preprocessing, n-gram models, word frequencies, and edit-distance algorithms can be used for autocomplete and autocorrect. Damerau–Levenshtein achieved better results than Levenshtein on the selected spelling test set.

Future improvements include independent evaluation, improved text cleaning, faster vocabulary searches, and context-aware language models.

## Project Structure
```text
Autocomplete-Autocorrect-Analysis/
├── Autocomplete_Autocorrect_Analysis.ipynb
├── README.md
└── dataset.csv  # Not included in the repository
```

## How to Run
1. Install Python and Jupyter Notebook.
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib nltk textdistance scikit-learn
   ```
3. Place the dataset CSV in the project folder.
4. Update the notebook's dataset file path.
5. Run the notebook cells in order.
