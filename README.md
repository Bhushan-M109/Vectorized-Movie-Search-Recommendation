# 🎬 Vectorized-Movie-Search-Recommendation

A machine learning–based movie recommendation engine that suggests films using **content similarity analysis**. It analyzes movie metadata such as genres, keywords, cast, and crew to recommend movies that are most similar to a selected title.

---

## 🚀 Overview
This system converts movie metadata into structured text features and transforms them into numerical vectors. By calculating similarity scores between these vectors, it identifies and recommends movies closest in content to the chosen film.

---

## 🛠 Tech Stack
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, AST  
- **Vectorization:** Bag of Words (CountVectorizer)  
- **Similarity Metric:** Cosine Similarity  

---

## 📊 Dataset
The project uses the **TMDB 5000 Movie Dataset**, containing metadata for ~4,800 movies, including:
- Genres  
- Keywords  
- Cast  
- Crew  
- Overview  

---

## ⚙️ How It Works

### 1. Data Preprocessing
- Merged movies and credits datasets  
- Removed missing values and duplicates  

### 2. Feature Engineering
Extracted key attributes:
- Top 3 cast members  
- Director  
- Genres and keywords  
- Cleaned and standardized text  

### 3. Tag Creation
All important textual features are combined into one column:
tags = overview + genres + keywords + cast + crew

### 4. Vectorization
- Converted tags into **5,000-dimensional vectors**
- Used CountVectorizer
- Removed English stop words  

### 5. Similarity Calculation
- Calculated cosine similarity between vectors  
- Returned closest matching movies  

---

## 🖥 Usage
Run the recommendation function:

```python
recommend("The Dark Knight Rises")
