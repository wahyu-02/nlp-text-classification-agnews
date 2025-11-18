# 📘 Comparative Study of FastText, Transformer, and LSTM for Text Classification Using GloVe Word Embedding on the AGNews Dataset

This repository contains the implementation and analysis of three different text classification methods—**FastText**, **Transformer**, and **LSTM**—using **GloVe word embeddings** on the **AGNews dataset**. The goal of this project is to compare performance, accuracy, computational efficiency, and resource usage across the three models.

---

# 📄 Research Paper

You can open the complete paper here:  
👉 **[Download / View Full Paper (PDF)](results/PERBANDINGAN METODE FASTTEXT, TRANSFORMER, DAN LSTM UNTUK KLASIFIKASI TEKS MENGGUNAKAN WORD EMBEDDING GLOVE PADA DATASET AGNEWS.pdf)**

Or view it directly in GitHub by clicking the file inside this repository:

`PERBANDINGAN METODE FASTTEXT, TRANSFORMER, DAN LSTM UNTUK KLASIFIKASI TEKS MENGGUNAKAN WORD EMBEDDING GLOVE PADA DATASET AGNEWS.pdf`

---

# 📚 Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methods](#methods)
  - [FastText](#1-fasttext)
  - [Transformer](#2-transformer)
  - [LSTM](#3-lstm)
- [Comparative Results](#comparative-results)
- [Conclusion](#conclusion)
- [Contributors](#contributors)

---

# 🔍 Introduction

Text classification plays an important role in Natural Language Processing (NLP).  
This project compares three well-known neural architectures:

- **FastText** (efficient bag-of-words style model)
- **LSTM** (sequential model capturing long-term dependencies)
- **Transformer** (attention-based model with strong contextual understanding)

All models use **pretrained GloVe word embeddings (100 dimensions)** and are tested on the **AGNews dataset**, combining both the *title* and *description* fields.

---

# 📁 Dataset

### AGNews Dataset
A widely used benchmark text classification dataset with 4 classes:
1. World  
2. Sports  
3. Business  
4. Science/Technology  

Each record contains:
- Title  
- Description  

Dataset is split into:
- Training set  
- Testing set  

---

# 🧠 Methods

## **1. FastText**

FastText represents text by averaging (mean pooling) all GloVe word embeddings in the sentence.  
It does **not** consider word order, making it lightweight and extremely fast.

### Implementation Summary
- Word Embedding: GloVe 100d (frozen)
- Mean pooling for sentence representation
- Fully connected classifier
- Optimizer: Adam
- Epochs: 10 — Batch size: 32

### Results
- **Accuracy:** 83%  
- **Macro F1:** 83%  
- Very fast training, low GPU usage  
- Weak in capturing complex semantic patterns  

---

## **2. Transformer**

Transformer leverages **self-attention** to capture global relationships across tokens.

### Implementation Summary
- GloVe embedding (100d), frozen
- Positional encoding added
- Transformer Encoder:
  - 2 layers
  - 4 attention heads
  - FFN size: 128
- Optimizer: Adam
- Epochs: 5 — Batch size: 32

### Results
- **Accuracy:** 90% (highest among all methods)
- **Macro F1:** 90%
- Excellent contextual understanding
- Moderate training time and memory usage  

---

## **3. LSTM**

LSTM is a recurrent neural network designed to handle sequential dependencies and long-term context.

### Implementation Summary
- GloVe embedding 100d, frozen
- LSTM hidden size: 128
- Dropout: 0.5
- Fully connected classifier
- Optimizer: Adam
- Epochs: 10 — Batch size: 32

### Results
- **Accuracy:** 84%
- **Macro F1:** 84%
- Good sequence comprehension
- Highest GPU memory usage  
- Struggles on Class 3 predictions (low recall)

---

# 📊 Comparative Results

## Accuracy Comparison
| Model        | Accuracy |
|--------------|----------|
| FastText     | 83%      |
| LSTM         | 84%      |
| **Transformer** | **90%** |

## Resource & Speed Comparison
| Model        | GPU Memory Usage | Training Speed |
|--------------|------------------|----------------|
| FastText     | Lowest           | Fastest        |
| Transformer  | Medium           | Moderate       |
| LSTM         | Highest          | Slowest        |

## Summary of Strengths
- **FastText** → Best for speed and efficiency  
- **LSTM** → Good for sequential patterns  
- **Transformer** → Best accuracy and generalization  

---

# 📝 Conclusion

- The **Transformer** outperforms all models with **90% accuracy**, thanks to self-attention.  
- **LSTM** performs well but requires more memory and struggles with difficult classes.  
- **FastText**, despite being simple, delivers competitive accuracy with extremely fast training.

Overall, the **Transformer is the best model**, while **FastText is ideal for resource-constrained environments**.

---

# 👥 Contributors
- **Hermalina Sintia Putri (121450052)**  
- **Veni Zahara Kartika (121450075)**  
- **Syifa Firnanda (121450094)**  
- **Silvia Azahrani (121450070)**  
- **Wahyudianto (121450040)**

---

