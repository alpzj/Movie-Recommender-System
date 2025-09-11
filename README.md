# 🎬 Movie Recommender System Using Machine Learning

This is a machine learning project to recommend movies based on content features like genres, keywords, cast, and crew using NLP techniques and similarity measures. The model is deployed using **Streamlit** and hosted on **Render**.

---

## 🚀 Demo

👉 [https://movie-recommender-system-dsg6.onrender.com]

---

## 📌 Project Overview

This project processes a dataset of movies and uses natural language processing (NLP) techniques to extract and combine relevant metadata such as genres, keywords, cast, and crew into a single text feature. The text data is vectorized and cosine similarity is computed to recommend movies similar to a user-selected movie. The recommendation system is deployed in a web application using **Streamlit**.

---

## 📁 Dataset

- Source: [TMDB 5000 Movie Dataset on Kaggle]
- Records: 4,803  
- Columns: `title`, `genres`, `keywords`, `cast`, `crew`, `overview`

---

## 🧹 Data Cleaning & Preprocessing

- Merged movies and credits datasets on `title`  
- Extracted important features: genres, keywords, top 3 cast members, director  
- Removed spaces in multi-word names for consistency  
- Created a combined `tags` feature by concatenating all text-based metadata  
- Lowercased all text for normalization  
- Removed stopwords and punctuation (optional)

---

## 📊 Exploratory Data Analysis (EDA)

- Analyzed distribution of movie genres  
- Visualized most common keywords and genres using word clouds  
- Examined counts of movies per director and top actors  
- Investigated popular genres and their frequency

---

## 🧠 Models & Techniques

- Used **CountVectorizer** with max_features=5000 and stop_words='english' for text vectorization  
- Calculated **cosine similarity** between movie vectors  
- Built a content-based recommender system returning top 5 most similar movies to input

---

## 🧪 Model Evaluation

- Recommendations validated through manual inspection of similarity  
- Similar movies share overlapping genres, cast, and plot elements  
- Tested on diverse movies to ensure relevant and meaningful suggestions

---

## 📦 Project Structure

```bash
├── app.py                # Streamlit application  
├── movie_list.pkl        # Movie metadata with combined tags  
├── similarity.pkl        # Cosine similarity matrix  
├── requirements.txt      # Python dependencies  
├── setup.sh              # Render deployment setup script  
├── Procfile              # Render deployment file  
├── .gitignore  
└── README.md             # Project documentation
