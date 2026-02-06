# GitHub Topic Recommendation using Extreme Multi-label Learning

## 📌 Overview
This project focuses on building an intelligent system to automatically recommend relevant topics for GitHub repositories. The system analyzes repository metadata such as repository name, description, and README content to predict multiple appropriate topics in large-scale label spaces.
              
The project addresses the challenge of **Extreme Multi-label Learning (XML)**, where the number of possible labels is very large and label distributions are highly imbalanced, including many rare or unseen labels.

---

## 🚀 Key Features
- Multi-label topic recommendation for GitHub repositories
- Scalable learning under extreme label settings
- Robust generalization to rare and unseen topics
- Integration of Large Language Models as auxiliary supervision

---

## 🧠 Methodology

### Extreme Multi-label Learning
We experiment with **ZestXML**, an XML algorithm designed to handle:
- Large label spaces
- Sparse and long-tail label distributions
- Zero-shot and generalized zero-shot settings

ZestXML leverages semantic representations of labels and instances to improve generalization beyond seen labels.

### LLM-as-a-Teacher Paradigm
To enhance training quality, we utilize an **LLM-as-a-Teacher** framework:
- Large Language Models are used to generate high-quality pseudo-labels from README content
- Repository READMEs are summarized to extract semantic signals
- Pseudo-labels are used to guide the training of bi-encoder models

This approach improves label coverage and semantic alignment between repositories and topics.

---

## 🗂️ Data
- GitHub repositories with metadata:
  - Repository name
  - Description
  - README content
- Topic labels provided by GitHub
- Data preprocessing includes text normalization, filtering noisy labels, and README summarization

---

## 📊 Evaluation
The system is evaluated using standard multi-label classification metrics:
- Precision@k
- Recall@k
- F1-score
- Performance on rare and unseen labels

Experimental results show that XML-based methods combined with LLM-generated supervision significantly improve topic recommendation quality.

---



