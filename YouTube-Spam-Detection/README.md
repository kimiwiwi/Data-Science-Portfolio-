# YouTube Spam Detection

## Overview
This project classifies YouTube comments as spam or not spam
using Text Mining and Logistic Regression.

## Dataset
- Source: YouTube Spam Collection Dataset
- Artist: Psy (Gangnam Style)
- Total data: 350 comments
- Target variable: CLASS (0 = not spam, 1 = spam)

## Text Processing Pipeline
| Step | Method |
|------|--------|
| Transformation | Lowercase |
| Tokenization | Regexp (\w+) |
| Normalization | Porter Stemmer |
| Filtering | Stop Words (English) |
| Vectorization | Bag of Words (Sublinear TF, IDF) |

## Model & Results
| Metric | Score |
|--------|-------|
| AUC | 0.981 |
| Accuracy | 94.3% |
| F1 Score | 0.943 |
| Precision | 0.949 |
| Recall | 0.943 |

## Conclusion
Logistic Regression successfully detects YouTube spam comments
with 94.3% accuracy. Key spam indicators include words like
"troll", "social", and "get".

## Tools
- Orange Data Mining
- Orange Text Mining Add-on
