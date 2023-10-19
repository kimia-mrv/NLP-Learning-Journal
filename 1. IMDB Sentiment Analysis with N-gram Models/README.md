# IMDB Sentiment Analysis with N-gram Models

## Overview
This repository contains the implementation of a sentiment analysis model for IMDB movie reviews using N-gram models. The goal is to classify movie reviews as positive or negative based on their content.

## Preprocessing
The text data undergoes several preprocessing steps:

1. Removal of punctuation, HTML tags, and links.
2. Elimination of non-alphabetic characters.
3. Lowercasing of all letters.
4. Removal of stopwords using the NLTK library.
5. Truncation of each review to a maximum of 500 characters.
6. Tokenization and stemming using NLTK.

## N-gram Model Construction
The code constructs N-gram language models (unigram, bigram, trigram, and 4-gram) based on the training data. The vocabulary is limited to the 3000 most frequent words, and the remaining words are replaced with `<unk>`. The implementation utilizes NLTK's n-gram generation capabilities.

## Probability Estimation and Perplexity
The models are trained using Laplace smoothing, and the perplexity is calculated for each model on both positive and negative datasets. The perplexity results indicate how well the models capture the language patterns of the given class.

### Preplexity Results:
- Positive Data:
  - Unigram: 565.38
  - Bigram: 288.56
  - Trigram: 2023.87
  - 4-gram: 3336.24
- Negative Data:
  - Unigram: 589.41
  - Bigram: 307.71
  - Trigram: 2147.40
  - 4-gram: 3412.68

## Model Evaluation
The accuracy of each N-gram model is evaluated on the test set:

- Unigram Accuracy: 81.98%
- Bigram Accuracy: 83.18%
- Trigram Accuracy: 75.43%
- 4-gram Accuracy: 67.01%

The bigram model achieves the highest accuracy, indicating its effectiveness in sentiment prediction.

## Prediction
The final prediction is performed using the bigram model, which demonstrated the best performance during evaluation.
