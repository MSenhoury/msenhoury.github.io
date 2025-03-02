---
title: "Learn NLP with Sentiment Analysis"
date: 2025-03-02
type: "docs"
math: true
tags:
  - NLP
  - AI
  - Machine Learning
  - Python
image:
  caption: "Master Natural Language Processing step by step."
bio: "Learn NLP concepts with hands-on sentiment analysis!"
---

# **Learn NLP with Sentiment Analysis** 🚀
A beginner-friendly introduction to **Natural Language Processing (NLP)**. Master **text processing, tokenization, and sentiment analysis** step by step!

---

## 🟢 **Lesson 1: What is NLP?**
Natural Language Processing (**NLP**) is a branch of Artificial Intelligence (AI) that enables computers to understand and process human language.

Mathematically, a sentence is a **sequence of words**:
\[
S = (w_1, w_2, w_3, ..., w_n)
\]
where \( w_i \) represents each word.

📝 **Examples of NLP applications:**
- **Chatbots** 🤖 (like ChatGPT)
- **Speech Recognition** 🎙 (Siri, Google Assistant)
- **Sentiment Analysis** 💬 (detecting positive/negative emotions in text)

---

## 🟢 **Lesson 2: Tokenization – Breaking Sentences into Words**
Tokenization is the process of **splitting text into individual words** or phrases.

📌 **Example: Tokenizing a sentence using Python**
```python
import nltk
nltk.download("punkt")

from nltk.tokenize import word_tokenize

sentence = "Natural Language Processing is amazing!"
tokens = word_tokenize(sentence)
print(tokens)
```
📝 **Mathematical Formula:**
\[
T(S) = \{ w_1, w_2, w_3, ..., w_n \}
\]
where each \( w_i \) is a token.

Example:
```
Input: "AI is awesome!"
Output: ['AI', 'is', 'awesome', '!']
```

---

## 🟢 **Lesson 3: Text Representation – Converting Words to Vectors**
Since machines cannot process raw text, we **convert words into numerical representations**.

### **🔢 One-Hot Encoding**
Each word is represented as a **binary vector** in a vocabulary of size \( V \):

| Word    | Vector Representation |
|---------|-----------------------|
| AI      | [1, 0, 0, 0, 0]       |
| is      | [0, 1, 0, 0, 0]       |
| cool    | [0, 0, 1, 0, 0]       |
| !       | [0, 0, 0, 1, 0]       |

📌 **Python Code:**
```python
from sklearn.preprocessing import OneHotEncoder
import numpy as np

words = np.array(["AI", "is", "cool", "!"]).reshape(-1, 1)
encoder = OneHotEncoder(sparse=False)
one_hot = encoder.fit_transform(words)
print(one_hot)
```
📝 **Mathematical Formula:**
\[
\text{one-hot}(w_i) = [0,0,...,1,...,0] \quad \text{(1 at index of } w_i \text{)}
\]

---

## 🟢 **Lesson 4: Sentiment Analysis with TextBlob**
Sentiment Analysis detects **positive, neutral, or negative emotions** from text.

📌 **Example: Using TextBlob for Sentiment Analysis**
```python
from textblob import TextBlob

text = "I love machine learning!"
analysis = TextBlob(text)
print(analysis.sentiment.polarity)  # Output: 0.5 (Positive)
```

📝 **Mathematical Formula for Sentiment Score:**
\[
S = \frac{\sum_{i=1}^{n} P(w_i)}{n}
\]
where \( P(w_i) \) is the **sentiment polarity** of each word \( w_i \) in the sentence.

**Interpretation of `sentiment.polarity` values:**
- **\( S > 0 \)** → Positive 😃
- **\( S = 0 \)** → Neutral 😐
- **\( S < 0 \)** → Negative 😠

---

## 🟢 **Lesson 5: Building a Custom Sentiment Classifier**
### **Step 1: Create a Training Dataset**
📌 **Example Dataset**
| Text                   | Sentiment |
|------------------------|----------|
| "I love this product"  | Positive |
| "This is terrible"     | Negative |
| "It's okay, not great" | Neutral  |

### **Step 2: Convert Text into Vectors (TF-IDF)**
Instead of one-hot encoding, we use **TF-IDF**:

\[
\text{TF-IDF}(w) = \text{TF}(w) \times \text{IDF}(w)
\]

where:
- **TF** (Term Frequency) measures how often a word appears.
- **IDF** (Inverse Document Frequency) gives less importance to common words.

📌 **Python Code**
```python
from sklearn.feature_extraction.text import TfidfVectorizer

texts = ["I love this product", "This is terrible", "It's okay, not great"]
vectorizer = TfidfVectorizer()
features = vectorizer.fit_transform(texts)
print(features.toarray())
```

---

## 🟢 **Lesson 6: Training a Sentiment Classifier**
Now, let's train a **machine learning model** for sentiment analysis!

📌 **Using Logistic Regression**
```python
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split

# Example dataset
texts = ["I love this product", "This is terrible", "It's okay, not great"]
labels = [1, 0, 0]  # 1 = Positive, 0 = Negative/Neutral

X_train, X_test, y_train, y_test = train_test_split(texts, labels, test_size=0.2)

vectorizer = TfidfVectorizer()
X_train_vectors = vectorizer.fit_transform(X_train)
X_test_vectors = vectorizer.transform(X_test)

model = LogisticRegression()
model.fit(X_train_vectors, y_train)

# Test the model
test_text = ["I hate this!"]
test_vector = vectorizer.transform(test_text)
prediction = model.predict(test_vector)

print("Predicted Sentiment:", "Positive" if prediction[0] == 1 else "Negative")
```

📝 **Mathematical Formula for Logistic Regression:**
\[
P(y=1 | x) = \frac{1}{1 + e^{-(w \cdot x + b)}}
\]

---

## 🎯 **Challenge: Build Your Own Sentiment Analysis Web App**
You can **deploy** your model using **Streamlit**!

📌 **Simple Web App Code:**
```python
import streamlit as st
from textblob import TextBlob

st.title("Sentiment Analysis App")
text = st.text_area("Enter a sentence:")
if st.button("Analyze Sentiment"):
    analysis = TextBlob(text)
    st.write("Polarity Score:", analysis.sentiment.polarity)
    if analysis.sentiment.polarity > 0:
        st.success("Positive Sentiment 😊")
    elif analysis.sentiment.polarity < 0:
        st.error("Negative Sentiment 😠")
    else:
        st.info("Neutral Sentiment 😐")
```

🔹 **Run the app**:
```sh
streamlit run app.py
```

---

## 🎉 **Congratulations! You Built a Sentiment Classifier!**
✅ You learned **NLP basics**  
✅ You built a **Sentiment Analysis model**  
✅ You trained a **Machine Learning classifier**  
✅ You created a **web app**  

🚀 **Next Steps:**
- **Fine-tune with more data**
- **Use deep learning models (`BERT`, `GPT-4`)**
- **Deploy it online (AWS, Hugging Face Spaces)**

📩 **Need help? Contact me at** [m.asenhoury@hotmail.com](mailto:m.asenhoury@hotmail.com)  
💡 **Follow my work on GitHub:** [github.com/mohamed-senhoury](https://github.com/mohamed-senhoury)
```
