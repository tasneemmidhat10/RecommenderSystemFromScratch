To make inference use the following python code: 
```python
import pickle
import numpy as np

# Load Model Weights
with open('users_latent_vectors.pkl', 'rb') as f: U = pickle.load(f)
with open('movies_latent_vectors.pkl', 'rb') as f: V = pickle.load(f)
with open('users_biases.pkl', 'rb') as f: b_u = pickle.load(f)
with open('item_biases.pkl', 'rb') as f: b_i = pickle.load(f)

GLOBAL_MEAN = 3.53  # Average rating of the dataset

def predict(user_id, movie_id):
    """Predicts rating for user_id on movie_id"""
    # Handle cold-start (unknown ID)
    if user_id >= len(b_u) or movie_id >= len(b_i):
        return GLOBAL_MEAN
        
    # Calculate score
    score = GLOBAL_MEAN + b_u[user_id] + b_i[movie_id] + np.dot(U[user_id], V[movie_id])
    return np.clip(score, 0.5, 5.0)

# Example: Predict rating for User 10 on Movie 500
print(f"Prediction: {predict(10, 500):.2f}")
```
