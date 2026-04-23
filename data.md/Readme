# Data Folder

This folder contains the datasets and supporting data required for the recommendation system.

## Files

* `ratings.csv`
  User–movie rating data

* `movies.csv`
  Movie metadata (title, genres)

## Required Structure

### ratings.csv

* `userId` → unique user identifier
* `movieId` → unique movie identifier
* `rating` → user rating (e.g., 1–5)

### movies.csv

* `movieId` → unique movie identifier
* `title` → movie title
* `genres` → movie categories

## Additional Inputs (Generated in Notebook)

* `cosine_sim` → similarity matrix used for content-based filtering
* `movie_indices` → mapping of movieId to matrix index

## How Data Is Used

1. `ratings.csv` is used to train the SVD model (collaborative filtering)
2. `movies.csv` is used to retrieve movie titles and genres
3. `cosine_sim` is used to compute similarity between movies
4. `movie_indices` links movie IDs to similarity matrix positions

## Notes

* Data must be loaded and preprocessed before model training
* Ensure column names match the expected format
* The similarity matrix must align with the movie dataset

## Integration

These datasets are required for:

* Running the recommendation notebook
* Feeding data into a dashboard or API
* Generating real-time recommendations
