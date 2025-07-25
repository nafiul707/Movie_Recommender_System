# 🎬 Movie Recommender System

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

## 📁 Folder & File Setup (Must Read)

The `app.py` file is located inside the `Front-End/` folder.  
To avoid path issues, you should also place the generated `.pkl` files there:

```
Front-End/
├── app.py
├── movie_list.pkl       ✅ place here after running the notebook
└── similarity.pkl       ✅ place here after running the notebook
```

You will get `movie_list.pkl` and `similarity.pkl` after running all cells in the notebook (`Movie_Recommender_System.ipynb`).  
If these files are placed elsewhere, the app **won’t work**.

🗂️ My Local Project Structure

```
Movie_Recommender_System/
├── Front-End/
│   ├── app.py
│   ├── movie_list.pkl
│   └── similarity.pkl
├── Movie_Recommender_System.ipynb
├── tmdb_5000_credits.csv
└── tmdb_5000_movies.csv
```

Keep this structure intact. If you shift or rename any file/folder, especially movie_list.pkl or similarity.pkl, the recommendation app will break due to missing dependencies.

---

## ▶️ Run the App

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)  
2. Run the notebook to generate `.pkl` files  
3. Move both `.pkl` files into the `Front-End/` folder  
4. In terminal:

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

