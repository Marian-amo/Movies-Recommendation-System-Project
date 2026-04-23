# Models Folder

This folder contains the saved model used in the recommendation system.

## Files

* `svd_model.pkl`
  Trained SVD model (Surprise) used to predict user ratings

## Required Inputs

To generate recommendations, the following inputs are required:

* `userId` (int) → target user
* `ratings` (DataFrame) → user-item interactions
* `movies` (DataFrame) → movie metadata
* `cosine_sim` (array) → precomputed similarity matrix
* `movie_indices` (mapping) → movieId to index mapping

## How It Is Used

1. Load the saved SVD model
2. Predict ratings for unseen movies
3. Combine predictions with cosine similarity scores
4. Rank movies and return Top-N recommendations

## Example

python id="g4w8qp"
import pickle

with open('models/svd_model.pkl', 'rb') as f:
    model = pickle.load(f)

model.predict(uid=1, iid=50)


## Notes

* The model is used together with additional data (ratings, similarity matrix)
* Ensure all inputs follow the same structure as used during training

## Integration

This model is designed to be used in:

* Dashboards 
* APIs (Flask/FastAPI)
* Recommendation pipelines
