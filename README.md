# 📰 News Topic Classification using DistilBERT

Automatically classify news articles into predefined categories using Machine Learning and Transformer-based Natural Language Processing.

---

## 📖 Introduction

News articles are published every second across thousands of websites worldwide. Automatically organizing these articles into meaningful categories improves search engines, recommendation systems, news aggregators, and digital libraries.

This project investigates two different approaches for multiclass news classification:

- Logistic Regression with TF-IDF features
- Fine-Tuned DistilBERT Transformer

The models are trained and evaluated on the **AG News Dataset**, allowing a direct comparison between traditional feature engineering and contextual language representations.

---

# 🎯 Problem Statement

Given the text of a news article, predict its correct category from four possible classes:

- 🌍 World
- 🏅 Sports
- 💼 Business
- 💻 Sci/Tech

---

# 📂 Dataset

Dataset Used

**AG News Dataset**

The dataset contains news articles collected from multiple publishers and grouped into four balanced categories.

### Data Preparation

- Balanced sampling
- Stratified train-validation split
- Short news articles
- Dynamic padding for transformers

---

# 🛠️ Models

## Baseline

### Logistic Regression

Feature Extraction

- TF-IDF
- Unigrams
- Bigrams

Advantages

- Fast
- Lightweight
- Easy to train

---

## Deep Learning Model

### DistilBERT

Pretrained Model

```
distilbert-base-uncased
```

Training Parameters

| Parameter | Value |
|-----------|---------|
| Epochs | 3 |
| Learning Rate | 3e-5 |
| Optimizer | AdamW |
| Padding | Dynamic |
| Evaluation | Macro Metrics |

---

# 💻 Technologies

Programming

- Python

Frameworks

- Hugging Face Transformers
- PyTorch
- Scikit-learn

Libraries

- NumPy
- Pandas
- Matplotlib
- Evaluate

---

# ⚙️ Workflow

```text
Load AG News Dataset
          │
          ▼
 Exploratory Analysis
          │
          ▼
 Text Preprocessing
          │
 ┌────────┴────────┐
 │                 │
 ▼                 ▼
TF-IDF         Tokenization
 │                 │
 ▼                 ▼
Logistic      DistilBERT
Regression    Fine-Tuning
 │                 │
 └────────┬────────┘
          ▼
     Model Evaluation
```

---

# 📊 Experimental Results

| Model | Accuracy | Precision | Recall | F1-score |
|--------|----------|-----------|--------|----------|
| Logistic Regression | 87.20% | 87.20% | 87.20% | 87.13% |
| DistilBERT | **92.20%** | **92.21%** | **92.20%** | **92.18%** |

---

# 🔍 Performance Discussion

### Logistic Regression

✔ Efficient training

✔ Good baseline

✘ Difficulty distinguishing similar news categories

---

### DistilBERT

✔ Better contextual understanding

✔ Higher multiclass accuracy

✔ Improved semantic representation

✔ Stronger generalization across categories

---

# 📁 Repository Structure

```
News-Topic-Classification/

│── LLM_Jayanth_.ipynb
│── README.md
│── requirements.txt
│── report.pdf

├── dataset/
│
├── notebooks/
│
├── models/
│
├── figures/
│     ├── class_distribution.png
│     ├── article_length.png
│     ├── confusion_matrix.png
│     └── accuracy_curve.png
│
└── outputs/
      ├── predictions.csv
      └── metrics.csv
```

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/news-topic-classification.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```bash
jupyter notebook
```

Open

```
LLM_Jayanth_.ipynb
```

---

# 📦 Python Requirements

```
transformers
datasets
torch
evaluate
accelerate
numpy
pandas
matplotlib
scikit-learn
```

---

# 📝 Sample Predictions

| News Headline | Predicted Category |
|---------------|-------------------|
| Government announces new economic reforms | Business |
| Local team wins championship title | Sports |
| Scientists discover new exoplanet | Sci/Tech |
| International leaders meet for climate summit | World |

---

# 🌟 Features

- Multiclass News Classification
- TF-IDF Feature Engineering
- Transformer Fine-Tuning
- Comparative Performance Analysis
- Confusion Matrix Evaluation
- Macro Precision, Recall & F1-score
- Contextual Language Understanding

---

# 🔮 Future Improvements

Future work could include:

- Training larger transformer models such as RoBERTa or DeBERTa
- Using multilingual news datasets
- Hyperparameter optimization
- Deploying the classifier as a web application
- Real-time news categorization API

---

# 📚 References

- AG News Dataset
- DistilBERT: Smaller, Faster, Cheaper and Lighter
- BERT: Pre-training of Deep Bidirectional Transformers
- Hugging Face Transformers
- Scikit-learn Documentation

---

# 👨‍💻 Author

**Lekkala Sai Jayanth**

MSc Data Science

University of Hertfordshire

---

# 📜 License

This repository is intended solely for educational and academic coursework purposes.
