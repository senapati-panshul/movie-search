Got it ✅ You want a **completely different README** so it doesn’t look similar at all. I’ll restructure it, change the writing style, simplify/expand where needed, and keep **only Windows commands** for clarity.

Here’s a fresh version:

````markdown
# 🎥 Movie Plot Semantic Search  

**Author**: Panshul Senapati (221020443, DSAI)  

This assignment demonstrates how to build a **semantic search engine** for movie plots. Instead of keyword matching, the system understands the *meaning* of queries using a transformer model (`all-MiniLM-L6-v2` from `SentenceTransformers`). The search retrieves the closest matches by computing similarity between query embeddings and movie plot embeddings.  

---

## 📝 Project Highlights
- Encoded movie plots into dense vectors using `all-MiniLM-L6-v2`  
- Compared embeddings with **cosine similarity** to measure relevance  
- Implemented a **command-line interface** to run searches from terminal  
- Added **unit tests** to check accuracy, result size, and similarity range  
- Provided a **toy dataset (`movies.csv`)** for quick testing  

---

## 📂 Files Included
- `movie_search.py` → main script containing semantic search logic  
- `movies.csv` → small dataset of movie titles and plots  
- `tests/test_movie_search.py` → unit tests for validation  
- `requirements.txt` → dependencies for running the project  
- `README.md` → documentation (this file)  

---

## ⚙️ Setup (Windows)

### 1. Clone the Repository
```powershell
git clone https://github.com/your-username/movie-semantic-search.git
cd movie-semantic-search
````

### 2. Create Virtual Environment

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

### 3. Install Required Packages

```powershell
pip install -r requirements.txt
```

---

## ▶️ Running the Program

Example search query:

```powershell
python movie_search.py --query "romantic drama with a twist" --top-n 3
```

The output will list the **top 3 most relevant movies** with their similarity scores.

---

## 🧪 Testing

Run the unit tests to verify everything is working:

```powershell
python -m unittest tests/test_movie_search.py -v
```

---

## 📌 Key Notes

* Model used: `sentence-transformers/all-MiniLM-L6-v2`
* Similarity metric: cosine similarity (range: 0 → 1)
* The first execution will take longer as the model is downloaded

---

## 🎯 Example

```powershell
python movie_search.py --query "spy thriller set in Paris" --top-n 2
```

Expected outcome: a spy-related movie should appear as the most relevant result.

---

## ❗ Troubleshooting

* **Model not found?** Ensure you are connected to the internet (the model downloads automatically on first run).
* **Virtual environment not activating?** Try:

```powershell
.\venv\Scripts\python.exe movie_search.py --query "romantic comedy" --top-n 2
```

---

✨ With this, you can semantically search through movie plots without relying on plain keywords.

