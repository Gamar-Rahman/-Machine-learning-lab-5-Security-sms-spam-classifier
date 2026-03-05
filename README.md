# -Machine-learning-lab-5-Security-sms-spam-classifier
Naive Bayes SMS spam classifier from scratch for smishing/phishing-style detection. Implements preprocessing, smoothing, log-trick, and ROC/AUC metrics.

# Naive Bayes SMS Spam Filter (From Scratch)

A cybersecurity-focused machine learning lab that implements **Naive Bayes classification from scratch** to detect **spam SMS messages**.  
This project mirrors real-world security use cases such as **phishing / smishing detection**, **SOC alert triage**, and **text-based threat filtering**.

## Why this matters for Cybersecurity
Spam SMS is a common delivery method for:
- credential theft (smishing)
- malicious links and payload delivery
- social engineering and fraud attempts

Building a baseline probabilistic classifier helps you understand how many security detection systems work under the hood before scaling to more advanced NLP/ML pipelines.

## Lab Highlights
✅ Implemented Bag-of-Words preprocessing:
- lowercasing
- punctuation removal
- tokenization
- word frequency counting

✅ Implemented Naive Bayes training **without using any off-the-shelf NB libraries**:
- prior probability `P(Y)`
- conditional probabilities `P(X|Y)` with **additive smoothing** (α=1, N=20000)
- handled unseen words using a required **"dummy"** probability entry

✅ Implemented prediction using **log-trick** to prevent numerical underflow:
- computes discriminant scores `g_y(x) = log P(y) + Σ log P(word|y)`
- outputs predicted label + posterior probabilities (softmax)

✅ Model evaluation:
- Accuracy
- Confusion Matrix
- F1 Score (important for imbalanced classes)
- ROC Curve + AUC

## Dataset
- SMS Spam Collection Dataset (UCI)
- ~5,572 messages with labels:
  - ham (0)
  - spam (1)

