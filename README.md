# 🧠 Depression Detection using LSTM (PyTorch)

This project is an NLP-based text classification model that detects whether a given Reddit post expresses signs of depression or not.

---

## 🚀 Project Overview

The goal of this project is to build a complete NLP pipeline from scratch, including:

- Data preprocessing & cleaning
- Handling missing values
- Balancing the dataset
- Tokenization & vocabulary building
- Sequence modeling using LSTM
- Model training & evaluation

---

## 📊 Dataset

- Source: Reddit posts dataset
- Features:
  - `title`
  - `body`
  - `label` (0 = Normal, 1 = Depression)

---

## 🧹 Data Preprocessing

- Combined `title` and `body` into a single text feature
- Removed:
  - URLs
  - Punctuation
  - Empty texts
- Converted text to lowercase
- Handled missing values
- Balanced dataset using downsampling

---

## 🔤 Text Processing

- Built custom vocabulary using word frequency
- Assigned:
  - `<PAD>` = 0
  - `<UNK>` = 1
- Converted text into sequences of integers
- Applied padding & truncation (fixed length)

---

## 🧠 Model Architecture

The model is built using PyTorch and includes:

- **Embedding Layer**
  - Converts words into dense vectors

- **LSTM Layer**
  - Captures sequential dependencies and context

- **Fully Connected Layer**
  - Maps features to output

- **Sigmoid Activation**
  - Outputs probability (0 → 1)

---

## ⚙️ Training Setup

- Loss Function: `Binary Cross Entropy (BCELoss)`
- Optimizer: `Adam`
- Batch Size: configurable
- Epochs: 3+

---

## 📈 Evaluation

- Accuracy Score
- Classification Report

---

## ⚠️ Challenges

- Data imbalance
- Noisy text data
- Handling unknown words
- Debugging model shapes and forward pass

---

## 🛠️ Tech Stack

- Python
- PyTorch
- Pandas
- NumPy
- Scikit-learn

---

## ▶️ How to Run

```bash
# Install dependencies
pip install torch pandas numpy scikit-learn

# Run the notebook or script
python main.py
