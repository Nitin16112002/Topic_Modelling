# Topic_Modelling

## 📌 Overview

This project uses **Latent Dirichlet Allocation (LDA)** to identify hidden topics within a collection of NPR news articles. By applying unsupervised machine learning techniques to textual data, the model reveals trends in politics, law enforcement, education, and public opinion.

---

## 💼 Business Problem

**How can media organizations better understand reader interests and content trends through automated topic discovery?**

By leveraging topic modeling, news platforms can:
- Gain insights into recurring themes in their content.
- Tailor articles to match audience interests.
- Identify underrepresented topics or overrepresented biases.

---

## 🛠️ Tech Stack

- **Python** 🐍  
- **Pandas** for data manipulation  
- **Scikit-learn** for LDA and preprocessing  
- **CountVectorizer** for building the document-term matrix  

---

---

## 🔍 Topic Modeling with LDA

```python
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.decomposition import LatentDirichletAllocation

# Vectorize the text
vectorizer = CountVectorizer(max_df=0.9, min_df=2, stop_words='english')
X = vectorizer.fit_transform(df['Article'])

# Fit LDA Model
model = LatentDirichletAllocation(n_components=4, random_state=42)
model.fit(X)

