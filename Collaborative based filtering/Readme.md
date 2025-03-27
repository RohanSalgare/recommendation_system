# Collaborative Filtering Recommendation System

## 📌 Overview
This project implements a **Collaborative Filtering Recommendation System** using **Centered Cosine Similarity**. The system suggests movies to users based on similar users' preferences (User-Based Filtering) by computing the centered mean for ratings and then finding similar users based on cosine similarity.
Centered cosine similarity, also known as the Pearson correlation coefficient, measures vector similarity by first centering the vectors (subtracting their means) and then calculating the cosine similarity

## 📂 Dataset
- The dataset used is `ratings_small.csv`.
- It contains **user ratings** for different movies.
- The data is structured as follows:
  ```csv
  userId,movieId,rating,timestamp
  1,31,2.5,1260759144
  1,1029,3.0,1260759179
  ```

## 🔍 Collaborative Filtering Method
### **User-Based Filtering**
- Computes the **centered mean** for user ratings.
- Calculates **cosine similarity** between users.
- Finds **5 most similar users** to the target user.
- Recommends **5 movies** highly rated by similar users that the target user hasn't watched.


## 📈 Performance Considerations
✅ Works well for **small datasets**.  
⚠️ **Not scalable** for large datasets. 

