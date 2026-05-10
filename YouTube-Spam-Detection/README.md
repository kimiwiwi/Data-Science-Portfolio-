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
| AUC | 0.983 |
| Accuracy | 94.3% |
| F1 Score | 0.943 |
| Precision | 0.949 |
| Recall | 0.943 |

## Analysis & Findings
The model successfully identified key patterns in spam comments:

1. **Self-promotion** - Words like "subscribe", "check", "channel"
   frequently appear in spam comments promoting other channels.

2. **External links** - Comments containing URLs and website
   references are strong indicators of spam.

3. **Engagement bait** - Words like "troll", "social", "get"
   are commonly used to lure users into clicking spam links.

## Conclusion
Logistic Regression with TF-IDF vectorization achieved 94.3%
accuracy in detecting spam comments. The high AUC score (0.983)
indicates the model excellently distinguishes spam from
legitimate comments, making it reliable for real-world
spam detection on YouTube comment sections.

## Tools
- Orange Data Mining
- Orange Text Mining Add-on
