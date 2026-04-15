# 📚 Goodreads Discovery Engine  
### Hybrid Book Recommendation System (Collaborative + Content-Based)

---

## 🚀 Problem Statement

With millions of books available, users struggle to discover relevant content. Traditional browsing often leads to poor engagement and missed opportunities.

This project builds a **hybrid recommendation system** that combines:
- User behavior (collaborative filtering)
- Book similarity (content-based filtering)

to deliver **personalized and scalable book recommendations**.

---

## 🧠 Solution Overview

We designed a multi-stage recommendation pipeline:
User / Book Input
↓
Collaborative Filtering (user similarity)
+
Content-Based Filtering (book similarity)
↓
Hybrid Score Combination
↓
Final Top-N Recommendations


---

## ⚙️ Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- TF-IDF (text vectorization)  
- Cosine Similarity  
- Jupyter Notebook  

---

## 📂 Project Structure

```
goodreads-discovery-engine/
│
├── data/                      # (ignored in GitHub)
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_collaborative_filtering.ipynb
│   ├── 03_content_based.ipynb
│   ├── 04_hybrid_model.ipynb
│   └── 05_cold_start.ipynb
│
├── README.md
└── .gitignore
```



---

## 🔍 Methodology

### 1. Exploratory Data Analysis (EDA)
- Analyzed rating distribution  
- Identified active users (≥20 ratings)  
- Filtered popular books (≥50 ratings)  
- Observed high sparsity in user-item matrix  

---

### 2. Collaborative Filtering
- Built user-item interaction matrix using pivot table  
- Used similarity-based approach (user-user similarity)  
- Recommended books liked by similar users  

---

### 3. Content-Based Filtering
- Used book metadata (title + description)  
- Applied TF-IDF vectorization  
- Computed cosine similarity between books  

---

### 4. Hybrid Model
- Combined:
  - Collaborative scores  
  - Content similarity scores  

Final Score = 0.6 * Collaborative + 0.4 * Content


- Improved recommendation relevance  

---

### 5. Cold Start Problem (New Users)
- New users have no history → collaborative filtering fails  
- Solution:
  - Take 3–5 liked books  
  - Recommend similar books using content similarity  

---

## 📊 Example Output

### Input:
User likes:

Harry Potter
Matilda

### Output:
Charlie and the Chocolate Factory
The Witches
Percy Jackson
Winnie-the-Pooh


---

## 📈 Key Insights

- Dataset is highly sparse (>99%), making recommendations challenging  
- Collaborative filtering alone is not sufficient  
- Content-based filtering helps solve cold start  
- Hybrid approach improves recommendation quality  

---

## ⚠️ Limitations

- Used sampled dataset for local execution  
- TF-IDF used instead of deep learning embeddings  
- No real-time deployment  

---

## 🔮 Future Improvements

- Use LightFM or deep learning-based models  
- Integrate FAISS for fast similarity search  
- Deploy as API (FastAPI/Flask)  
- Build UI for interaction  

---

## ▶️ How to Run

Install dependencies:
pip install pandas numpy scikit-learn matplotlib seaborn


Run notebooks in order:


01_eda.ipynb
02_collaborative_filtering.ipynb
03_content_based.ipynb
04_hybrid_model.ipynb
05_cold_start.ipynb


---

## 💡 Key Features

✔ Hybrid recommendation system  
✔ Cold start handling  
✔ Explainable recommendations  
✔ End-to-end pipeline  

---

## 🧾 Resume Highlights

- Built hybrid recommendation system combining collaborative and content-based filtering  
- Designed cold-start solution using content similarity  
- Handled sparse datasets and built scalable recommendation pipeline  

---

## 🔥 Final Note

This project demonstrates a complete understanding of recommendation systems, including real-world challenges like sparsity and cold start, along with practical implementation.