# Movies-Recommendation-System-Project
A movie recommendation system built using the MovieLens dataset that suggests top movies to users based on their ratings using collaborative filtering and 


##  Project Overview
This project builds a **movie recommendation system** using both:
- Collaborative Filtering (SVD)
- Content-Based Filtering (TF-IDF)

These approaches are combined into a **hybrid model** to improve recommendation quality and address real-world challenges such as the cold-start problem.

---

##  Business Problem
Streaming platforms need to recommend relevant content to users. However:
- New users have little interaction data  
- New movies may not have ratings  
- Single-model systems are limited  

This project develops a **hybrid recommendation system** that balances:
- Personalization (user preferences)
- Content similarity (movie features)

---

##  Data Understanding
The dataset includes:
- User ratings  
- Movie titles  
- Genres  
- Tags  

### Key Steps:
- Data loading and inspection  
- Handling missing values  
- Removing duplicates  
- Exploratory analysis (rating distributions, sparsity)

---

##  Data Preparation
- Merged ratings and movie metadata  
- Filtered low-activity users and movies  
- Created combined text features (genres + tags)  

---

##  Modeling

### 1. Baseline Model
- Simple collaborative filtering benchmark  

### 2. SVD Model
- Matrix factorization using Singular Value Decomposition  
- Captures latent relationships between users and movies  

### 3. Tuned SVD Model
- Hyperparameter tuning applied  
- Improved performance across evaluation metrics  

---

## Model Evaluation
Models were evaluated using:
- RMSE (Root Mean Squared Error)  
- MAE (Mean Absolute Error)  
- Precision  

 **Tuned SVD achieved the best predictive performance**

---

## Content-Based Filtering (TF-IDF)
- Applied TF-IDF to genres and tags  
- Converted text into numerical vectors  
- Used cosine similarity to measure movie similarity  

 Purpose:
- Recommend similar movies  
- Handle the cold-start problem  

---

## Hybrid Recommendation System

The hybrid model combines:
- Predicted ratings (SVD) → personalization  
- Similarity scores (TF-IDF) → content relevance  

##  Hybrid Model Insights
- Tested different alpha values
- Observed how recommendations change:
  - Lower α → more similarity-based  
  - Higher α → more personalized  

---

## Recommendation Functions

### Collaborative Filtering
- Recommends unseen movies using tuned SVD  

### Hybrid Model
- Combines SVD predictions with TF-IDF similarity  
- Produces more balanced recommendations  

---

## Results & Insights
- Tuned SVD improved prediction accuracy  
- TF-IDF enabled content-based similarity  
- Hybrid model provided a more flexible and robust system  

---

## Limitations
- TF-IDF depends on quality of text data  
- Hybrid model requires tuning (alpha selection)  
- Evaluation differs between ranking and prediction tasks  

---

## Future Improvements
- Use advanced NLP techniques (e.g., embeddings)  
- Improve feature engineering  
- Explore deep learning recommendation models  
- Deploy as a web application  

---
[Tableau](https://public.tableau.com/app/profile/sonia.cherop/viz/IMDBMovieRatingsandViewershipDashboard/IMBDMOVIERATINGSDASHBOARD)

## Conclusion
This project demonstrates that:
- Model tuning significantly improves performance  
- Collaborative filtering alone is not sufficient  
- Content-based methods help solve cold-start problems  
- Hybrid models provide a more practical real-world solution 

 ## Technologies Used
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Surprise (SVD)  
- TF-IDF (NLP)  
- Tableau  


 # Setup Instructions
1. Clone the repository
git clone https://github.com/Marian-amo/Movies-Recommendation-System-Project

2. Create a virtual environment (recommended)
 python -m venv venv


3. Install dependencies
pip install -r requirements.txt

4. Download Dataset
https://grouplens.org/datasets/movielens/

5. Run Jupyter Notebook
jupyter notebook
Open:notebook.ipynb 


