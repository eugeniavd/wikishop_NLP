# Toxic Comment Detection for Wikishop

The online store Wikishop is launching a new service that allows users to edit and supplement product descriptions, similar to wiki communities. In other words, customers can suggest edits and comment on changes made by others.

To support this feature, the store needs a tool that can detect toxic comments and send them for moderation.

The goal of this project was to train a model that classifies comments as toxic or non-toxic, and ensure it reaches an F1 score of at least 0.75.

## Dataset Description
toxic_comments.csv — the main dataset

text — the user-generated comment

toxic — target label (1 if the comment is toxic, 0 otherwise)

## Task
Develop a model that classifies comments as toxic or non-toxic.

Evaluate performance using the F1-score.

Target performance: F1 ≥ 0.75.

## Project Plan
1. Data loading and inspection

2. Text preprocessing

 - Lowercasing

- Removing non-Latin characters and digits

- Removing stopwords

- Lemmatization

- Removing multiple whitespaces

3. Feature engineering

- Basic features (text length, word count, etc.)

- TF-IDF vectorization

- Doc2Vec embeddings

- BERT embeddings

4. Model training

Logistic Regression on:

- Raw text (TF-IDF)

- Text + engineered features

- BERT embeddings

5. Evaluation on validation and test sets

## Results
- Original dataset: F1 = 0.76

- Dataset with additional features: F1 = 0.78

- BERT: F1 = 0.89

A robust preprocessing pipeline was developed. Multiple models were compared, and the use of BERT embeddings significantly improved performance.

The final model meets the business requirement and can be integrated into the Wikishop comment moderation system.



