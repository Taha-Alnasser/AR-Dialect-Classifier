# Arabic Dialect Classification

This repository contains a project on written Arabic dialect classification across five regional varieties using multiple modeling approaches. The goal is to compare classical machine learning, neural networks, and pretrained language models on the same task.

## Models

The project evaluates three approaches:

Logistic regression using TF IDF unigram and bigram features as a strong baseline  
A convolutional neural network implemented in PyTorch and trained from scratch  
A zero shot classifier based on a pretrained XLM Roberta model adapted for Arabic  

## Results

| Model | Accuracy | Macro F1 |
|------|----------|----------|
| Logistic Regression | 0.76 | 0.71 |
| CNN | 0.642 | 0.563 |
| XLM Zero Shot | 0.21 | 0.168 |

The logistic regression model performed best. The CNN struggled due to limited data, and the zero shot model performed poorly without task specific training.

## Repository Contents

AR_Classifier_4521.ipynb  
Single Google Colab notebook containing all preprocessing, training, and evaluation code. Running all cells reproduces the results.

Dialect_Classifier_CSCI4521.pdf  
Full project report with detailed methodology and analysis.

AR_Classifier_Poster.pptx  
Project poster summarizing the work.

## How to Run

Open AR_Classifier_4521.ipynb in Google Colab and run all cells in order. The notebook includes comments that explain each section.

## Notes

This project focuses on experimentation rather than deployment. Tokenization is done using simple whitespace splitting, and the dataset size limits neural model performance.
