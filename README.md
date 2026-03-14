# fakereviewdetect
A Hybrid Deep Learning Architecture for Fake Review Detection Combining Textual and Sentiment Features
# Hybrid Deep Learning Architecture for Fake Review Detection

## Overview

This project presents a **Hybrid Deep Learning approach for detecting deceptive online reviews** using textual and sentiment-based features. The system integrates multiple deep learning architectures including **BiLSTM, BiLSTM with Attention, Hybrid Sentiment Models, and Transformer-based models (BERT)** to analyze and classify reviews as **fake or genuine**.

The main objective is to evaluate how combining **textual representations and sentiment features** improves the performance of fake review detection systems.

---

## Problem Statement

Online platforms such as e-commerce websites and review portals are increasingly affected by **fake or deceptive reviews**, which can mislead consumers and damage trust in digital marketplaces.

Traditional machine learning methods often struggle to capture the **contextual semantics and emotional exaggeration patterns** commonly present in fake reviews. This project proposes a **hybrid deep learning framework** to address these challenges.

---

## Key Features

* Deep learning-based **fake review classification**
* Hybrid architecture combining **textual features and sentiment polarity**
* Comparative analysis of multiple models
* Use of **transformer-based contextual embeddings**
* Visualization of model performance

---

## Dataset

The experiments were conducted using a **Fake Reviews Dataset** containing over **40,000 reviews** with the following attributes:

| Column      | Description                                  |
| ----------- | -------------------------------------------- |
| review_text | Text content of the review                   |
| rating      | Star rating associated with the review       |
| label       | Classification label (0 = Genuine, 1 = Fake) |

The dataset was preprocessed using text normalization, stop-word removal, and tokenization before training the models.

---

## Methodology

### 1. Data Preprocessing

The preprocessing pipeline includes:

* Lowercasing text
* Removing punctuation and special characters
* Removing stopwords
* Tokenization
* Padding sequences for deep learning models

---

### 2. Word Representation

Text was converted into numerical vectors using:

* **Word embeddings**
* **GloVe pretrained embeddings**
* **Transformer-based embeddings (BERT)**

These embeddings allow the models to capture semantic relationships between words.

---

### 3. Models Implemented

#### 1. BiLSTM Model

A **Bidirectional Long Short-Term Memory network** processes text sequences in both directions to capture contextual dependencies.

Architecture:

```
Embedding → BiLSTM → Dense → Sigmoid
```

---

#### 2. BiLSTM + Attention Model

An **Attention mechanism** was added to highlight important words in reviews.

Architecture:

```
Embedding → BiLSTM → Attention → Dense → Output
```

---

#### 3. Hybrid Model (Text + Sentiment)

The hybrid architecture combines **deep textual features** with **sentiment polarity features** extracted using TextBlob.

Architecture:

```
Review Text → BiLSTM → Attention
                         ↓
                  Text Representation
                         +
                 Sentiment Polarity
                         ↓
                  Feature Concatenation
                         ↓
                   Dense Layer
                         ↓
                     Output
```

---

#### 4. Transformer Model (BERT)

A **BERT-based transformer model** was used for contextual text classification. BERT captures deep semantic relationships within reviews and achieved the best performance.

Architecture:

```
Review Text → BERT Encoder → Classification Layer → Output
```

---

## Results

| Model              | Accuracy  |
| ------------------ | --------- |
| BiLSTM             | 91.0%     |
| BiLSTM + Attention | 90.9%     |
| Hybrid Model       | 91.2%     |
| BERT               | **93.5%** |

The results demonstrate that **transformer-based models outperform traditional deep learning architectures**, while hybrid models provide improvements by incorporating sentiment features.

---

## Conclusion

This study demonstrates that deep learning techniques are highly effective for detecting deceptive online reviews. The hybrid architecture improves performance by integrating **textual and sentiment-based features**, while **BERT achieves the highest accuracy due to its contextual understanding of language**.

Future work may explore:

* Graph Neural Networks for reviewer behavior analysis
* Multimodal fake review detection
* Domain adaptation for cross-platform review datasets

---

## Technologies Used

* Python
* TensorFlow / Keras
* PyTorch
* HuggingFace Transformers
* NLTK
* TextBlob
* Scikit-learn
* Pandas & NumPy

---

## Applications

* E-commerce review filtering
* Reputation management systems
* Social media moderation
* Consumer trust analysis

---

## Author

Mahak Taneja
