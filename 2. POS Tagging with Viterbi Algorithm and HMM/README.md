# Part-of-Speech Tagging with Viterbi Algorithm and Hidden Markov Model

## Overview
This repository implements a Part-of-Speech (POS) tagging solution using the Viterbi algorithm and a Hidden Markov Model (HMM). The task involves assigning POS tags to words in a given text, where each tag represents a specific grammatical category (e.g., noun, verb, adjective).

## Dataset
The training dataset contains labeled sentences in Persian, where each word is tagged with its corresponding POS category. The goal is to train an HMM on this dataset to predict POS tags for unseen text.

### Dataset Statistics
- Number of POS tags: 23
- Training set word count: 18,949
- Validation set word count: 16,235
- Test set word count: 10,594
- Out-of-vocabulary words in validation set: 8,927
- Out-of-vocabulary words in test set: 4,971

## Implementation Details
The implementation utilizes the following libraries:
- `collections`: for counting occurrences
- `numpy`: for mathematical and matrix operations
- `nltk`: for generating n-grams

### Hidden Markov Model (HMM)
1. **Vocabulary Selection:**
   - The 8,000 most frequent words in the training set are chosen as the vocabulary.
   - The remaining words are replaced with `<unk>`.

2. **N-gram Generation:**
   - Sentences are tokenized using `<s>` for the start and `</s>` for the end of each sentence.
   - N-grams are generated for bigram model.

3. **Probability Estimation:**
   - Transition and emission probabilities are calculated using add-k smoothing.

4. **Viterbi Algorithm:**
   - The Viterbi algorithm is applied to find the most likely sequence of POS tags for a given input sentence.

## Model Evaluation
The accuracy of each model is evaluated on both the training and validation sets for different values of k.

| k      | 10^-8 | 10^-5 | 10^-4 | 10^-3 | 10^-2 | 10^-1 | 1     |
|--------|-------|-------|-------|-------|-------|-------|-------|
| Train  | 95.8% | 95.8% | 95.8% | 95.8% | 95.8% | 95.6% | 94.7% |
| Validate | 91.9% | 91.9% | 91.8% | 91.7% | 91.4% | 91.2% | 92.5% |

The best validation accuracy is achieved when k=1.

## Discussion
1. The model exhibits overfitting on the training data as k decreases, leading to decreased performance on the validation set.
2. The optimal value for k is selected based on the best performance on the validation set (k=1).

## Prediction
For predicting POS tags on new data, the model with k=1 is selected for its superior performance on the validation set.
