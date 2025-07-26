# 🧠 NLP Text Preprocessing Techniques

This project demonstrates Natural Language Processing (NLP) techniques for preprocessing textual data. Using Python and the NLTK (Natural Language Toolkit) library, it covers essential steps such as tokenization, punctuation removal, lemmatization, and emoji handling—critical components in building reliable NLP pipelines.

---

## 📌 Objective

To preprocess raw textual data in a structured way, enabling better performance for downstream tasks such as text classification, sentiment analysis, and information retrieval.

---

## 🔍 Key Features

- **Tokenization**
  - Word-level tokenization using `nltk.word_tokenize`
  - Sentence-level tokenization using `nltk.sent_tokenize`

- **Punctuation Removal**
  - Filtering out common punctuation using custom logic

- **Lemmatization**
  - Converting words to their base form using `WordNetLemmatizer`

- **Emoji Handling**
  - Translating emojis to human-readable text using the `emoji` library (`emoji.demojize`)

---

## ⚙️ Installation

Ensure you have the required libraries installed:

```bash
pip install nltk emoji
````

Download essential NLTK resources:

```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
nltk.download('stopwords')  # Optional, for stopword removal if extended
```

---

## 🧪 Sample Usage

### Lemmatization Example

```python
from nltk.stem import WordNetLemmatizer
from nltk.tokenize import word_tokenize

lemmatizer = WordNetLemmatizer()
text = "He was running and eating at the same time."
tokens = word_tokenize(text)
tokens = [word for word in tokens if word.isalnum()]

lemmatized_words = [lemmatizer.lemmatize(word) for word in tokens]
print(lemmatized_words)
```

---

## 📁 Project Structure

```
NLP_TextPreprocessing_Basic.ipynb  # Jupyter notebook containing all preprocessing steps
Datasets                           # CSV files uesd in this project
README.md                          # Project documentation
```

---

## 💡 Best Practices Noted

* Avoid modifying lists during iteration; use list comprehensions instead.
* Always download and verify NLTK resources before calling functions.
* Modular approach to text cleaning enhances maintainability and scalability.
