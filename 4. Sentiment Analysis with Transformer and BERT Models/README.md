# Sentiment Analysis with Transformer and BERT Models

This repository contains the implementation of sentiment analysis using Transformer and BERT models. The primary goal is to analyze and compare the performance of these models on an IMDB movie review dataset.

## Introduction

Sentiment analysis is a natural language processing task that involves determining the sentiment expressed in a piece of text. This repository explores the application of Transformer and BERT models for sentiment analysis on the IMDB movie review dataset. The notebook (`src.ipynb`) presents the entire pipeline, including data preprocessing, model training, and evaluation.

## Dataset

The IMDB movie review dataset is used for this task. It includes unsupervised data, training, validation, and test sets. The dataset is available in the `IMDB` directory.

## Preprocessing

Data preprocessing is a crucial step in any NLP task. The notebook covers various preprocessing steps, including:

- Tokenization
- Text cleaning
- Byte Pair Encoding (BPE) Tokenization

## Transformer Encoder

The notebook implements a Transformer Encoder model for sentiment analysis. It includes hyperparameter tuning and training. Overfitting issues are addressed, and different model configurations are explored.

## BERT

The BERT section of the notebook includes:

### Self-Supervised Pre-training

This step involves self-supervised pre-training of the BERT model. It covers:

- Masking input tokens
- Forward and backward passes
- Loss computation

### Fine-tuning

The pre-trained BERT model is fine-tuned for sequence classification, specifically for sentiment analysis on the IMDB dataset. The notebook includes freezing pre-trained weights and compiling the model.

### Further Fine-tuning

Additional fine-tuning steps are performed to improve the model's performance. It includes:

- Changing masking probability
- Monitoring overfitting
- Saving the best-performing model

## Results

The results section covers model evaluations and predictions.

### Evaluation

The notebook evaluates the trained models on different datasets, including:

- Unsupervised data
- Validation data
- Test data

Model performance metrics such as loss and accuracy are reported.

