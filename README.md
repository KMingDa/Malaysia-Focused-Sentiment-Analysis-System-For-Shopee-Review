# Malaysia-Focused-Sentiment-Analysis-System-For-Shopee-Review

A Natural Language Processing (NLP) project that classifies customer reviews into **Positive, Neutral, and Negative sentiments**.

This project explores different text representation techniques and machine learning models, including traditional machine learning approaches and advanced Transformer-based models. A user-friendly sentiment prediction interface was also developed using **Gradio**.

---

# 📌 Project Overview

The objective of this project is to build a sentiment classification system that can automatically analyse user reviews and determine their emotional polarity.

The project pipeline includes:

1. Data Collection
2. Text Pre-processing
3. Knowledge Representation
4. Model Training and Evaluation
5. Sentiment Prediction Demo

---

# 🛠️ Technologies Used

## Programming Language
- Python

## Libraries & Frameworks

### Data Processing
- Pandas
- NumPy
- NLTK

### Machine Learning
- Scikit-learn

### Word Representation
- TF-IDF
- Word2Vec

### Deep Learning / Transformer Models
- Hugging Face Transformers
- PyTorch

### Deployment Interface
- Gradio

---

# 📂 Dataset

The dataset contains user reviews with corresponding sentiment labels.

## Classes

| Label | Description |
|------|-------------|
| Positive | Positive opinions or satisfaction |
| Neutral | Neither positive nor negative |
| Negative | Negative opinions or complaints |

---

# 🔄 NLP Pre-processing Pipeline

The following preprocessing techniques were applied:

1. **Data Cleaning**
   - Removed duplicated reviews
   - Removed missing values
   - Removed invalid entries

2. **Language Translation**
   - Malay and Chinese reviews were translated into English

3. **Text Cleaning**
   - Lowercase conversion
   - URL removal
   - HTML removal
   - Number removal
   - Character normalization

4. **Tokenization**

5. **POS Tagging**

6. **Lemmatization**

7. **Stop-word Removal**
   - Removed common English stop words
   - Kept negation words (`not`, `no`, `nor`) because they affect sentiment meaning

---

# 🧠 Knowledge Representation

Two traditional text representation approaches were implemented:

## 1. TF-IDF

TF-IDF represents each review using the importance of words within the corpus.

Features:
- Unigram and bigram features
- Sparse vector representation
- Vocabulary learned from training data only

---

## 2. Word2Vec

Word2Vec converts words into dense numerical vectors based on semantic similarity.

Configuration:

| Parameter | Value |
|-----------|-------|
| Vector Size | 100 |
| Window Size | 5 |
| Minimum Count | 2 |
| Epochs | 100 |

Document representation was generated using mean pooling of word embeddings.

---

# 🤖 Models Implemented

## Traditional Machine Learning Models

| Feature Representation | Models |
|-----------------------|--------|
| TF-IDF | Multinomial Naive Bayes |
| TF-IDF | Logistic Regression |
| TF-IDF | Linear SVM |
| TF-IDF | Random Forest |
| Word2Vec | Gaussian Naive Bayes |
| Word2Vec | Logistic Regression |
| Word2Vec | Linear SVM |
| Word2Vec | Random Forest |

---

## Transformer Models

Fine-tuned Transformer-based models:

- BERT (`bert-base-uncased`)
- DistilBERT (`distilbert-base-uncased`)
- RoBERTa (`roberta-base`)

---

# 📊 Model Performance

## Best Traditional Model

| Model | Representation | Accuracy |
|------|----------------|----------|
| Linear SVM | TF-IDF | 82.54% |

## Best Overall Model

| Model | Accuracy |
|------|----------|
| RoBERTa | 88.89% |

RoBERTa achieved the highest performance due to its ability to capture contextual word meanings and complex language patterns.

---

# 🎨 Sentiment Analysis Demo

A Gradio-based web interface was developed for real-time sentiment prediction.

Features:

- User enters a review
- Text is automatically translated into English
- RoBERTa predicts sentiment
- Displays:
  - Predicted sentiment
  - Confidence score
  - Probability distribution for each class


Example output:

```
😊 POSITIVE

Confidence: 95.23%

Positive: 95.23%
Neutral : 3.10%
Negative: 1.67%
```

---

# 🚀 How to Run

## 1. Run Notebook

Open:

```
Source Codes.ipynb
```

Run all cells sequentially:

1. Data preprocessing
2. Knowledge representation
3. Model training
4. Model evaluation
5. Gradio deployment

---

## 👥 Contributors

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/KMingDa">
        <img src="https://avatars.githubusercontent.com/KMingDa" width="100px;" alt="KERK MING DA"/><br />
        <sub><b>KERK MING DA</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/1211209221">
        <img src="https://avatars.githubusercontent.com/1211209221" width="100px;" alt="Benjamin"/><br />
        <sub><b>Benjamin</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/yapmengyoon">
        <img src="https://avatars.githubusercontent.com/yapmengyoon" width="100px;" alt="Yap Meng Yoon"/><br />
        <sub><b>Yap Meng Yoon</b></sub>
      </a>
    </td>
  </tr>
</table>

---
