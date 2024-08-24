# SMS Spam/Ham Classification

This project focuses on the classification of SMS messages as either spam or ham (non-spam), a common problem in Natural Language Processing (NLP). The model utilizes the Bag of Words model (sparse vector matrix) and compares the performance of Gaussian Naive Bayes and Multinomial Naive Bayes algorithms.

## Problem Overview

The SMS Spam/Ham classification task involves determining whether a given SMS message is spam (unwanted or unsolicited messages) or ham (legitimate communication). This classification is critical for filtering out spam messages in SMS applications.

### Dataset

The dataset used in this project contains labeled SMS messages, with each message categorized as either spam or ham. The goal is to build a model that can accurately predict the label of new, unseen messages.

### Techniques Used

- **Bag of Words:** A representation of text data that maps words to vectors based on their frequency in the document.
- **Naive Bayes Classifiers:**
  - **Gaussian Naive Bayes:** Assumes that features follow a normal distribution.
  - **Multinomial Naive Bayes:** Assumes that features follow a multinomial distribution, making it more suitable for text classification.

## Model Comparison

The project compares the performance of Gaussian Naive Bayes and Multinomial Naive Bayes. The results clearly indicate that Multinomial Naive Bayes is better suited for text classification:

### Classification Report

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| **0 (Ham)** | 1.00 | 0.99 | 0.99 | 857 |
| **1 (Spam)** | 0.97 | 0.99 | 0.98 | 289 |
| **Overall Accuracy** | | | **0.99** | 1146 |
| **Macro Avg** | 0.98 | 0.99 | 0.99 | 1146 |
| **Weighted Avg** | 0.99 | 0.99 | 0.99 | 1146 |

- **Misclassified SMS Messages:** 13 out of 1,146

The classification report shows that the model has a high precision, recall, and F1-score, particularly for the ham class. The Multinomial Naive Bayes classifier achieved an overall accuracy of 99%.

## Potential Improvements

While the current model performs well, further improvements could be made by implementing **Term Frequency-Inverse Document Frequency (TF-IDF)**. TF-IDF adjusts the Bag of Words model by considering the importance of words in the context of the entire corpus, reducing the weight of common words that may not be as informative.
Likewise using the Complement NB algorithm may improve performance due to imabalanced dataset. 

## Conclusion

The SMS Spam/Ham classification model, using Multinomial Naive Bayes, effectively classifies messages with high accuracy. The model's performance could be further enhanced with techniques like TF-IDF to improve the representation of text data.
