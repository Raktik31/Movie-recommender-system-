# 🎬 Movie Recommender System  

This project is a **content-based movie recommender system** that suggests movies similar to the one selected by the user.  
It uses **cosine similarity** on preprocessed movie feature vectors and displays movie posters using the **TMDB API**.  
The interactive interface is built with **Streamlit**.  

---

## 📊 Data Exploration & Understanding  

1. **Dataset**  
   - We worked with a dataset of movies (movie titles, IDs, and metadata).  
   - The dataset was preprocessed and saved into two files:  
     - `movie_list.pkl` → contains movie titles and IDs.  
     - `similarity.pkl` → precomputed similarity matrix for fast recommendations.  

2. **Exploration Highlights**  
   - Each movie is represented by numerical vectors based on its features (genre, overview, cast, crew, keywords).  
   - Using **cosine similarity**, we can compute how close one movie is to another.  
   - Example: Movies like *Inception* are closer to *Interstellar* and *The Prestige* than to *Toy Story*.  

---

## ⚙️ How the Recommendation Works  

1. **User Input**: You select a movie from the dropdown in the Streamlit app.  
2. **Find Index**: The system locates the index of that movie in `movie_list.pkl`.  
3. **Similarity Check**: Looks up the corresponding row in `similarity.pkl` to find similar movies.  
4. **Top Results**: Picks the top 5 most similar movies.  
5. **Posters**: Fetches posters from the **TMDB API** and displays them alongside movie titles.
   **Project Structure:**
   movie-recommender/
│-- app.py               # Main Streamlit application
│-- movie_list.pkl       # Pickle file containing movie data
│-- similarity.pkl       # Pickle file containing similarity matrix
│-- requirements.txt     # List of dependencies
│-- README.md            # Project documentation

**Technologies Used**

Python → Core programming language

pandas, numpy, scikit-learn → Data handling and similarity calculation

Streamlit → Web interface for easy interaction

Requests → Fetch posters via TMDB API

Developed by **Raktik Ghosh**



