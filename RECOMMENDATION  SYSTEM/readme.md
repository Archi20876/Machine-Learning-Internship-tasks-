Company: CODTECH IT solutions

Name: Archita Paul

Intern ID:CITSOD42

Domain: Machine Learning

Duration: 4 weeks

Mentor: Neela Santosh

### RECOMMENDATION SYSTEM USING COLLABORATIVE FILTERING OR MATRIX FACTORIZATION TECHNIQUES.

1. Data Loading and Exploration
The project uses two datasets:

* pvr.csv: Contains movie IDs and corresponding titles.
* ratin.csv: Includes user ratings with columns userId, movieId, and rating.

The data was loaded using pandas, and the structure was examined to understand the number of users, movies, and ratings. A pivot table was created to represent the user-movie matrix with movie IDs as rows and user IDs as columns.

2. Data Preprocessing
* To handle missing ratings, all NaN values were filled with zero.
* To ensure quality recommendations and reduce noise, the dataset was filtered:
Only movies rated by more than 10 users were retained.
Only users who rated more than 50 movies were kept.

This step helped reduce sparsity and focused the model on active users and popular movies.

3. Sparsity Handling
A sample matrix was used to demonstrate sparsity by calculating the ratio of zero vs non-zero entries.The final user-item matrix was then converted into a compressed sparse row (csr_matrix) format using SciPy to optimize memory usage and improve computational efficiency.

4. KNN Model for Recommendations
The K-Nearest Neighbors algorithm was implemented using sklearn.neighbors.NearestNeighbors.Cosine similarity was used as the distance metric.The model was trained on the sparse user-item matrix.

A custom function get_recommendation() was defined to:

* Accept a movie title input, locate its movieId,

* Use the KNN model to find the top 10 similar movies,

* Return recommendations along with similarity scores.

5. Visualization
* Two scatter plots were created using Matplotlib to visualize:

* The number of users who rated each movie, with a red threshold line at 10.

* The number of ratings per user, with a green threshold line at 50.
  
* These plots helped validate the filtering criteria and show the distribution of user interactions.

6. Interactive Gradio Interface
To make the system user-friendly, a web-based interface was developed using Gradio.The user inputs a movie title.The interface displays the top 10 recommended movies.This provides an intuitive and fast way to test the recommendation engine without diving into the code.

7. Evaluation and Output
Although the system doesn't use explicit accuracy metrics (since it's unsupervised), its performance is validated by the relevance of movie recommendations.Test predictions were shown for a sample input like "Avatar", returning a list of 10 closely related movies.
