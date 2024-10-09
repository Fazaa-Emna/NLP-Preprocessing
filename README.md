# Sentiment Analysis on IMDB Movie Reviews with TF-IDF and Text Preprocessing

## Overview
This project performs **sentiment analysis** on the **IMDB Movie Reviews** dataset using machine learning techniques. The goal is to classify movie reviews as either positive or negative based on the text data. The project follows a comprehensive workflow that includes **data exploration**, **data cleaning**, **text preprocessing** steps like tokenization, lemmatization, handling negations, and custom stop word removal, followed by **TF-IDF vectorization** for feature extraction.

## Features
- **Data Exploration**: Basic analysis of the IMDB dataset to understand the distribution of reviews and key statistics.
- **Data Cleaning**:
    - **Expand Contractions**: Convert contractions (e.g., "don't") to their expanded forms ("do not").
    - **Lowercase Text**: Convert all text to lowercase for uniformity.
    - **Remove HTML Tags**: Strip out HTML content.
    - **Remove URLs**: Eliminate web addresses.
    - **Remove Non-ASCII Characters**: Remove emojis and other non-standard characters.
    - **Remove Punctuation**: Remove punctuation marks.
    - **Remove Numbers**: Remove numerical digits.
    - **Remove Extra Whitespace**: Clean up irregular spacing.
- **Tokenization**: Split the cleaned text into individual tokens (words).
- **Handling Negations**: Combine negation words with the following token (e.g., "not good" → "not_good").
- **Lemmatization**: Reduce words to their base forms (e.g., "running" → "run").
- **Custom Stop Word Removal**: Remove custom stop words that do not contribute meaning to the review.
- **Reconstructing Final Text**: Rebuild the preprocessed tokens into the final cleaned text.
- **TF-IDF Vectorization**: Convert preprocessed text into numerical vectors using Term Frequency-Inverse Document Frequency (TF-IDF) for use in machine learning algorithms.

## Dataset: IMDB Movie Reviews
The dataset used in this project is the **IMDB Movie Reviews** dataset, which contains **50,000 movie reviews** labeled as either positive or negative. It is a widely-used dataset for binary sentiment classification.

- **Number of reviews**: 50,000
- **Positive reviews**: 25,000
- **Negative reviews**: 25,000
- **Dataset source**: [IMDB Movie Reviews Dataset]([https://ai.stanford.edu/~amaas/data/sentiment/](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/data))

## Project Workflow

### 1. Data Exploration
Initial exploration of the dataset includes checking class distribution (positive vs. negative reviews), basic statistics, and visualizing word frequencies.

### 2. Data Cleaning
The raw text data contains noise such as HTML tags, URLs, punctuation, numbers, and extra whitespace. We perform the following steps to clean the data:

- **Expand Contractions**: Convert contractions like "can't" into "cannot" to ensure accurate interpretation of negations.
- **Lowercase Text**: Convert all reviews to lowercase to ensure consistency during tokenization.
- **Remove HTML Tags**: Strip away unnecessary HTML content, as it's irrelevant for sentiment analysis.
- **Remove URLs**: Remove web links and URLs that might appear in the reviews.
- **Remove Non-ASCII Characters**: Eliminate emojis and other characters that don’t contribute to the text meaning.
- **Remove Punctuation**: Remove punctuation marks like periods and commas.
- **Remove Numbers**: Exclude numbers from the reviews since they don’t affect sentiment.
- **Remove Extra Whitespace**: Clean up irregular spacing after text transformations.

### 3. Tokenization
We split each cleaned review into individual tokens (words). This allows us to process each word in isolation and prepare for further text transformations.

### 4. Handling Negations
To preserve the meaning of negations, we combine negation words (e.g., "not", "no", "never") with the words they modify. For example, "not good" becomes "not_good", which allows the model to better capture the sentiment.

### 5. Lemmatization
Lemmatization reduces words to their base or root form. For example:
- "running" → "run"
- "better" → "good"

This helps ensure that different forms of the same word are treated as the same during analysis.

### 6. Custom Stop Word Removal
We remove commonly used words that do not add significant meaning to the sentiment, such as "the", "is", "in", etc. We also create a custom list of stop words tailored to the dataset.

### 7. Reconstructing the Final Preprocessed Text
After tokenization and lemmatization, we reconstruct the cleaned text by joining the tokens back into sentences. This version of the text is ready for vectorization.

### 8. TF-IDF Vectorization
We use **TF-IDF (Term Frequency-Inverse Document Frequency)** vectorization to convert the preprocessed text into numerical features. TF-IDF measures how important a word is to a document relative to the dataset.

## Contributing
Feel free to contribute to this project by submitting a pull request or reporting issues.


