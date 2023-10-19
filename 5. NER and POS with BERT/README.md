
# Named Entity Recognition (NER) and Part-of-Speech (POS) with BERT

This repository contains a project focused on Named Entity Recognition (NER) and Part-of-Speech (POS) tasks using BERT-based models from TensorFlow and Hugging Face.

## Preprocessing

In the preprocessing step, the text is segmented into sentences and labels are aligned with segmented sentences. The BERT tokenizer (`bert-base-cased`) is employed for tokenization with a maximum length of 128 tokens. The tokenizer splits each word into multiple tokens, and to handle this, a new label list is created for each sample.

## Model Architecture

The project adopts a pre-trained BERT model (`bert-base-cased`). Softmax layers are added for both Named Entity Recognition (NER) and Part-of-Speech (POS) prediction. The model is trained using SparseCategoricalCrossentropy loss with a learning rate of 0.0001.

## Training

The model undergoes training for 10 epochs with a batch size of 64. Notably, the learning rate plays a crucial role in model performance. A learning rate of 1e-3 resulted in poor performance, while a learning rate of 1e-4 achieved over 90% accuracy and was selected for the final predictions.

## Evaluation

NER and POS tasks are evaluated with metrics including accuracy, recall, precision, and F1-score. Validation set results are as follows:

### NER Metrics:
- Accuracy: 0.9887
- Recall: 0.9887
- Precision: 0.9887
- F1-score: 0.9887

### POS Metrics:
- Accuracy: 0.9617
- Recall: 0.9617
- Precision: 0.9617
- F1-score: 0.9617
