# Information Retrieval System with TF-IDF and LSI

## Overview
This repository implements an Information Retrieval (IR) system using the TF-IDF (Term Frequency-Inverse Document Frequency) vectorization method and Latent Semantic Indexing (LSI). The goal is to retrieve relevant documents from a corpus given a user query.

## Libraries Used
- `numpy`: for numerical operations
- `nltk`: for natural language processing tasks
- `sklearn`: for machine learning algorithms
- `matplotlib`: for plotting graphs
- `tabulate`: for creating tables

## Preprocessing
The preprocessing includes tokenization, stemming, and stop-word removal. The NLTK library is used for these tasks.

## TF-IDF Vectorization
The TfidfVectorizer from scikit-learn is employed to convert the text data into TF-IDF matrices. This is crucial for capturing the importance of words in the documents.

## Latent Semantic Indexing (LSI)
LSI is implemented using the TruncatedSVD algorithm from scikit-learn. It reduces the dimensionality of the TF-IDF matrices to capture latent semantic structures.

## Evaluation Metrics
The system is evaluated based on precision, recall, and F1-score. These metrics help assess the performance of the retrieval system.

## Results
The relationship between precision and recall is observed. As the number of retrieved documents increases, precision decreases while recall increases. The F1-score is considered for selecting an optimal number of retrieved documents, emphasizing a balance between precision and recall.

\
| number of related documents extracted | Precision | Recall | F1-Score |
| ------------------------------------ | --------- | ------ | -------- |
| 5                                    | 0.278788  | 0.129577 | 0.176923 |
| 10                                   | 0.230303  | 0.214085 | 0.221898 |
| 20                                   | 0.166667  | 0.309859 | 0.216749 |
| 40                                   | 0.111364  | 0.414085 | 0.175522 |


## Evaluation
Evaluate the system's performance using precision, recall, and F1-score metrics. Adjust parameters as needed for optimal retrieval results.

## Visualization
Use Matplotlib to visualize the precision-recall trade-off for different numbers of retrieved documents.

## Conclusion
This IR system demonstrates the effectiveness of TF-IDF and LSI in retrieving relevant documents. The evaluation metrics provide insights into the system's performance, guiding further optimizations.
