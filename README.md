# 📊 Topic Analysis of Review Data

This project performs topic modeling on customer reviews for the **Lenovo K8 smartphone**, uncovering common issues, opinions, and themes using Natural Language Processing (NLP) techniques. The goal is to extract latent topics from review text using the **Latent Dirichlet Allocation (LDA)** algorithm.

---

## 📑 Table of Contents
- [Project Objective](#project-objective)
- [Dataset Description](#dataset-description)
- [Tech Stack & Libraries](#tech-stack--libraries)
- [Workflow](#workflow)
  - [1. Data Loading](#1-data-loading)
  - [2. Text Preprocessing](#2-text-preprocessing)
  - [3. Tokenization & Lemmatization](#3-tokenization--lemmatization)
  - [4. Topic Modeling (LDA)](#4-topic-modeling-lda)
  - [5. Coherence Score](#5-coherence-score)
  - [6. Topic Visualization](#6-topic-visualization)
- [Key Results](#key-results)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [How to Run](#how-to-run)

---

## 🎯 Project Objective

To explore **hidden topics** within customer reviews of the Lenovo K8 by applying:
- Unsupervised learning
- Natural Language Processing (NLP)
- Topic modeling with LDA

This helps businesses understand user concerns and product feedback more clearly.

---

## 📄 Dataset Description

- **Filename:** `K8 Reviews v0.2.csv`
- **Columns:**
  - `sentiment`: 1 = Positive, 0 = Negative
  - `review`: User-submitted free text

---

## 🛠️ Tech Stack & Libraries

- **Python**
- **Pandas** – Data handling
- **NLTK** – Stopword removal, lemmatization
- **Gensim** – Dictionary, Corpus, LDA modeling
- **Matplotlib** – Data visualization
- **Regular Expressions** – Text cleanup

---

## 🔁 Workflow

### 1. Data Loading
- Loaded CSV file using `pandas.read_csv`.
- Inspected dataset using `.head()` and `.info()`.

### 2. Text Preprocessing
- Converted text to lowercase.
- Removed punctuation, digits, and special characters using `re`.
- Removed stopwords using NLTK’s stopword list.
- Discarded words with length ≤ 3 characters.

### 3. Tokenization & Lemmatization
- Split sentences into individual words (tokens).
- Applied `WordNetLemmatizer` to reduce words to their base form.
- Final output: list of clean, meaningful words per review.

### 4. Topic Modeling (LDA)
- Created a **dictionary** and **corpus** using Gensim.
- Built an **LDA model** to extract topics from the processed data.
- Tuned the number of topics manually for better interpretability.

### 5. Coherence Score
- Calculated coherence score using `gensim.models.CoherenceModel`.
- Used this score to assess the **quality and relevance** of topics.

### 6. Topic Visualization
- Printed the top words contributing to each topic.
- Topics were interpreted manually based on frequent terms.

---

## 📈 Key Results

- Multiple distinct topics were identified from review data.
- Example themes include:
  - Battery life issues
  - Performance problems
  - Positive mentions of display and price
- These topics reflect the most commonly discussed concerns or praises.

---

## 📌 Conclusion

- The LDA model successfully uncovered **grouped themes** in the dataset.
- Proper preprocessing improved topic clarity and coherence.
- Topic modeling helped summarize long user reviews into digestible insights.
