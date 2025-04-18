# CodeX AI Technical Assessment

This project classifies sentences as **Greeklish** (Greek written in Latin characters) or **English** using real-world scraped data and a Logistic Regression model.

---

## 📁 Files Overview

- `main.ipynb` – Complete pipeline: scraping, preprocessing, training, evaluation  
- `model/` – Trained model and TF-IDF vectorizer  
- `initial_dataset.csv` – Raw data  
- `preprocessed_sentences.csv` – Cleaned data  
- `requirements.txt` – Dependencies  
- `Documentation.pdf` – Full project explanation  

---

## 📊 Data Sources

**Greeklish**  
- Reddit (`r/greece`)  
- Insomnia.gr Forum  
- YouTube Comments (`_akH1Bns2B8`)  

**English**  
- Reddit (`r/AskReddit`)  
- Wikipedia (AI article)  

---

## 🧹 Preprocessing Steps

- Lowercasing  
- Sentence splitting (., !, ?)  
- Special character and digit removal (regex)  
- Tokenization using NLTK  
- Stopword removal  
- Rebuilding cleaned sentences  

---

## 🤖 Model Details

- **Classifier:** Logistic Regression  
- **Vectorizer:** TF-IDF (max 5000 features)  
- **Train/Test Split:** 80/20 (stratified)  

### 📈 Evaluation Results

- **Accuracy:** 93.22%  
- **Precision:** 94.18%  
- **Recall:** 93.22%  
- **F1-Score:** 93.27%  

---

## 🧪 Prediction Example

```python
predict_text("ti kaneis")  # → "Greeklish"
predict_text("Hello, how are you?")  # → "English"
