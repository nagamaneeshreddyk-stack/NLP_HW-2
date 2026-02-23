# NLP_HW-2
#Student
- K. Naga Maneesh Reddy
- ID: 700773566


## 📌 Overview
This repository contains my solutions and Python implementations for NLP Homework‑2, covering:
- Naive Bayes document classification
- Harms of classification
- Bigram language models
- Zero‑probability and smoothing
- Trigram backoff
- Confusion matrix evaluation
- Python implementations for bigram models and evaluation metrics
All code is written in Python and fully reproducible.

## 📚 Training Corpus
The model is trained on the following sentences:
`<s> I love NLP </s>`
`<s> I love deep learning </s>`

`<s> deep learning is fun </s>`


These sentences form the basis for all unigram and bigram counts.

## 🛠️ Features
Unigram & Bigram Counting
The program extracts:
- unigram_counts: total occurrences of each word
- bigram_counts: total occurrences of each adjacent word pair
MLE Probability Estimation
Bigram probabilities are computed using:
P(w_2\mid w_1)=\frac{\mathrm{count}(w_1,w_2)}{\mathrm{count}(w_1)}
Sentence Scoring
A function multiplies the bigram probabilities across a sentence to compute its overall likelihood.
Model Comparison
Two test sentences are evaluated to determine which one the model prefers.

## 🚀 How It Works
1. Counting
The model scans the corpus and builds:
- Unigram counts (e.g., I → 2, love → 2, deep → 2)
- Bigram counts (e.g., ('I','love') → 2, ('deep','learning') → 2)
2. Probability Calculation
Example:
If "I" appears 2 times and "I love" appears 2 times:
P(\mathrm{love}\mid I)=\frac{2}{2}=1.0
3. Sentence Evaluation
The model evaluates:
- S1: `<s> I love NLP </s>`
- S2: `<s> I love deep learning </s>`

## 📊 Results
|  |  | 
| `<s> I love NLP </s>` |  | 
| `<s> I love deep learning </s>` |  | 


Conclusion
The model prefers S1, because it has a higher cumulative probability.
S2 contains more bigrams, and multiplying more probabilities (each ≤ 1) reduces the total score.

## 📦 Included Python Code
The repository includes:
- Unigram and bigram counting
- MLE probability computation
- Sentence probability function
- Sentence comparison logic
All code is clean, readable, and ready to run.

## ✔️ Summary
This project demonstrates:
- How to build a statistical bigram language model
- How to compute unigram and bigram counts
- How to estimate bigram probabilities using MLE
- How to evaluate and compare sentence probabilities
It serves as a foundational example of classical NLP language modeling.
