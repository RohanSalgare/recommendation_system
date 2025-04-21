# Hybrid Recommendation System

## 📌 Overview
This project implements a **Hybrid Movie Recommendation System** that combines **Collaborative Filtering** and **Content-Based Filtering** using a weighted approach. The goal is to provide personalized movie recommendations by analyzing both user behavior and movie attributes.

### 🔧 Key Techniques Used
- **User-Based Collaborative Filtering** using Cosine Similarity
- **Content-Based Filtering** using movie similarity (e.g., genres)
- **Hybrid Score Calculation**: Weighted combination of collaborative and content scores

## 📂 Dataset
- **ratings_small.csv**: Contains user ratings for movies
- **movies.csv**: Contains metadata for each movie (e.g., title, genre)

### Example from `ratings_small.csv`:
```csv
userId,movieId,rating,timestamp
1,31,2.5,1260759144
1,1029,3.0,1260759179
```

## 💡 Use Cases
- Personalized movie recommendations
- Enhancing user engagement on movie platforms
- Cold-start problem mitigation with hybrid methods

## 🚀 How It Works

### ✅ Collaborative Filtering
- Finds users similar to the target user (via cosine similarity of rating vectors)
- Recommends movies liked by those similar users

### ✅ Content-Based Filtering
- Computes similarity between the target movie and movies the user has already watched
- Recommends movies that are most similar to user preferences

### ✅ Hybrid Approach
- The function `hybrid_recommend(user_id, movie_id, alpha=0.5)`:
  - Calculates a **collaborative score** based on similar users’ ratings
  - Calculates a **content score** based on similarity between movies
  - Combines both scores using the formula:
    ```python
    final_score = alpha * collab_score + (1 - alpha) * content_score
    ```

## 📦 Installation & Usage

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/hybrid-recommender.git
cd hybrid-recommender
```

### 2. Install Dependencies
```bash
pip install pandas numpy scikit-learn
```

### 3. Run the Notebook
```bash
jupyter notebook
```

### 4. Sample Usage
```python
recommend_movies(user_id=1, top_n=5)
```

## 📈 Performance Considerations
- Efficient for small to mid-sized datasets
- Can be scaled using sparse matrices and model-based filtering (e.g., SVD, ALS)



