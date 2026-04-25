# Mini BERT Pretraining: NSP & MLM

## 📌 Overview

This project implements a **Mini BERT-style transformer model** designed for pretraining with two fundamental self-supervised learning tasks:

- **Masked Language Modeling (MLM)**
- **Next Sentence Prediction (NSP)**

The system replicates the core ideas behind modern transformer-based language models while using a **lightweight and efficient architecture** suitable for fast experimentation and practical understanding of pretraining dynamics.

The implementation focuses on building a complete pipeline—from data preparation to model training—demonstrating how bidirectional contextual representations are learned from raw text.

---

## ⚙️ Key Capabilities

- Transformer encoder-based Mini BERT architecture
- Dual pretraining objectives (MLM + NSP)
- Token masking strategy for contextual prediction learning
- Sentence-pair classification for coherence modeling
- Modular and extensible design
- Efficient training on limited compute resources
- Fully customizable architecture depth and embedding size

---

## 🧠 Core Concepts Implemented

### 🔹 Masked Language Modeling (MLM)

The model randomly masks a percentage of input tokens and learns to predict them using surrounding context.

Example:
Input: I love [MASK] learning
Target: deep


This enables the model to learn **bidirectional context understanding**.

---

### 🔹 Next Sentence Prediction (NSP)

The model predicts whether two sentences are logically consecutive in a document.

Example:
Sentence A: The transformer architecture is powerful.
Sentence B: It has changed modern NLP systems.
Label: IsNext ✔️

Sentence A: I like machine learning.
Sentence B: The weather is very hot today.
Label: NotNext ❌


---

## 🏗️ Model Architecture

The Mini BERT model is composed of:

- Token Embedding Layer
- Positional Encoding Layer
- Segment (Sentence) Embeddings
- Multi-layer Transformer Encoder
- MLM Prediction Head (token-level classification)
- NSP Prediction Head (binary classification)

---

## 🔁 Training Pipeline

The training process follows these steps:

1. Text preprocessing and tokenization
2. Construction of sentence pairs for NSP
3. Random token masking for MLM
4. Forward pass through transformer encoder
5. Joint optimization of MLM + NSP losses
6. Backpropagation and parameter updates

Total loss:
Loss = MLM_Loss + NSP_Loss


---

## 🔧 Configuration Highlights

You can control model behavior through configurable parameters:

- Number of transformer layers
- Hidden size / embedding dimension
- Attention heads
- Masking probability
- Batch size and learning rate
- Sequence length

---

## 📊 Features

- Joint MLM + NSP training objective
- Efficient transformer encoder implementation
- Flexible dataset pipeline
- Custom tokenizer support
- Scalable architecture for experimentation
- Clean separation of model and training logic

---

## 🚀 Future Extensions

- Replace NSP with Sentence Order Prediction (SOP)
- Integration with large-scale corpora
- Support for HuggingFace transformer compatibility
- Distributed training support
- Attention visualization tools
- Model compression and distillation variants

---

## 🧪 Output Goals

After training, the model learns:

- Context-aware token predictions
- Sentence relationship understanding
- Strong bidirectional language representations

---

