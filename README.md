# 🎬 Movie Recommendation System

A content-based movie recommender system built with Python and Streamlit. It helps users discover movies similar to their favorites using metadata like cast, crew, genres, and keywords.

---

## 📦 Dataset

Due to GitHub’s file size restrictions, the dataset is **not included** in this repo.

📥 **Download the dataset from Kaggle**:  
[TMDB Movie Metadata Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

After downloading:
- Place `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv` in the project root (or wherever your notebook expects them).
- Run the notebook (`Movie_Recommender_System.ipynb`) to generate the `.pkl` files.

---

## 🧠 How It Works

- Extracts features from metadata (`overview`, `cast`, `crew`, `keywords`, etc.)
- Transforms them using `CountVectorizer`
- Computes similarity using cosine distance
- Returns top recommended movies based on similarity score

---

## 📁 Important Notes on File Paths

The deployed Streamlit app (`app.py`) resides in the `Front-End/` folder.  
Make sure to place the generated `.pkl` files inside this folder **exactly like this**:

```
Front-End/
├── app.py
├── movie_list.pkl       ✅ Must be here
└── similarity.pkl       ✅ Must be here
```

If the `.pkl` files are elsewhere, the app **will not run** properly.

---

## ▶️ Running the App

1. Make sure `movie_list.pkl` and `similarity.pkl` are inside `Front-End/`
2. Open terminal in `Front-End/`
3. Run:

```bash
streamlit run app.py
```

---

## 🛠️ Built With

- Python
- Pandas, NumPy
- scikit-learn
- Streamlit

---

## 👤 Author

Developed by [Nafiul Islam](https://github.com/nafiul707)

