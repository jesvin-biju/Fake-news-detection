
#  Fake News Detection using Machine Learning  

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)  
![Scikit-Learn](https://img.shields.io/badge/ML-Scikit--Learn-orange)  
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)  
![Accuracy](https://img.shields.io/badge/Accuracy-~99%25-success)  

---

##  Overview  

This project detects whether a news article is **Fake  or Real** using Machine Learning.  
It uses **TF-IDF vectorization** and compares two models:

-  Logistic Regression  
-  Random Forest  

---

##  Demo  

```python
predict_news("Breaking shocking truth they don’t want you to know")
```

### Output:
```
Logistic Regression: Fake
Random Forest: Fake
```

---

## Models Used  

###  Logistic Regression  
- Fast and stable  
- Works well with high-dimensional text data  
- Lower False Positives (safer for fake news detection)  

###  Random Forest  
- Ensemble of decision trees  
- Captures complex patterns  
- Slightly higher accuracy  

---

##  Results  

| Model | Accuracy | F1 Score |
|------|---------|---------|
| Logistic Regression | 98.87% | 98.96% |
| Random Forest | 98.96% | 99.05% |

---

##  Key Insight  

Although Random Forest has slightly higher accuracy, **Logistic Regression is preferred** because it produces fewer false positives (fake news classified as real), making it safer.

---

##  Methodology  

### 1. Data Preprocessing  
- Combine `title + text`  
- Remove duplicates  
- Shuffle dataset  

### 2. Feature Extraction  
- TF-IDF Vectorizer  
- n-grams (1,2)  
- Max features: 10,000  

### 3. Train-Test Split  
- 80% training  
- 20% testing  
- Stratified  

### 4. Model Training  
- Logistic Regression  
- Random Forest  

### 5. Evaluation  
- Accuracy  
- F1 Score  
- Confusion Matrix  
- Cross-validation  

---

##  Model Saving (PKL)

```python
import pickle

# Save model
pickle.dump(model, open("model.pkl", "wb"))

# Load model
model = pickle.load(open("model.pkl", "rb"))
```

---

##  Project Structure  

```
Fake-News-Detection/
│
├── Fake.csv
├── True.csv
├── model.pkl
├── vectorizer.pkl
├── main.ipynb
└── README.md
```

---

##  Technologies Used  

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  

---

##  Key Learnings  

- TF-IDF is powerful for text data  
- Logistic Regression works very well for NLP  
- F1 Score is important along with accuracy  
- False positives are critical in fake news detection  

---

---

