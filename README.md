# 🎬 Movie Recommendation System

This is a content-based movie recommender system built using Python. It helps users discover movies similar to their favorites based on metadata like cast, crew, genres, and keywords.

## 📦 Project Access

Due to GitHub file size limits, the full project is uploaded as a ZIP file.  
➡️ **[Download and extract `Movie_Recommender_System.zip`](./Movie_Recommender_System.zip)**

Once extracted:
- Open `Movie_Recommender_System.ipynb`
- Run the notebook in Jupyter or Google Colab
- Ensure all CSV files are in the same folder

---

## 🧠 How It Works

1. Merge and clean metadata from TMDB datasets
2. Extract relevant features (overview, cast, crew, genres)
3. Vectorize using `CountVectorizer`
4. Compute similarity using cosine distance
5. Serve results via a simple Streamlit front-end

---

## 🗂️ Folder Structure

```
Movie_Recommender_System/
├── Movie_Recommender_System.ipynb       # Main logic & model
├── Front-End/
│   ├── app.py                           # Streamlit UI
│   ├── movie_list.pkl                   # ⬅️ Generated after running notebook
│   └── similarity.pkl                   # ⬅️ Generated after running notebook
├── tmdb_5000_credits.csv
├── tmdb_5000_movies.csv
└── README.md
```

⚠️ `movie_list.pkl` and `similarity.pkl` will be created automatically **after you run all cells in the Colab/Jupyter notebook**. Place both inside the `Front-End` folder before launching the app.

---

## ▶️ Running the App

After generating the `.pkl` files:

```bash
cd Front-End
streamlit run app.py
```

---

## 🛠️ Tech Used

- Python
- Pandas, NumPy
- scikit-learn
- Streamlit

---

## 👤 Author

Developed by [Nafiul Islam](https://github.com/nafiul707)
