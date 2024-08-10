# Movies Recommendations

This project implements a movie recommendation system using both Content-Based Filtering and Collaborative Filtering techniques. The system leverages data from two datasets: one containing user ratings for various movies and another with movie titles and their corresponding IDs.

# 1. Data Preprocessing
First, we preprocess the data by loading the datasets into pandas dataframes and merging them based on a common column (item_id). This combined dataset allows us to link user ratings with specific movie titles, making it easier to analyze the data and build the recommendation models.

# 2. Data Visualization
We visualize the distribution of movie ratings to understand the overall rating patterns. This helps in identifying trends, such as how often certain ratings are given by users. A histogram is used to plot the frequency of different rating values.

# 3. Content-Based Filtering
For content-based recommendations, the system analyzes movie titles. By using a technique called TF-IDF (Term Frequency-Inverse Document Frequency), we convert movie titles into numerical vectors that represent the importance of each word in the title relative to the entire dataset.

Cosine Similarity is then computed between these vectors to measure how similar one movie is to another based on their titles.
Using this similarity measure, the system can recommend movies that are most similar to a given movie title.

# 4. Collaborative Filtering
Collaborative filtering is used to recommend movies based on the preferences of similar users. The approach can be broken down into the following steps:

User-Item Matrix: We create a matrix where each row represents a user, and each column represents a movie. The values in the matrix are the ratings given by users to movies.

SVD (Singular Value Decomposition): To reduce the dimensionality of the matrix and capture the underlying structure of the data, we apply SVD. This helps in identifying latent features that influence user preferences.

Cosine Similarity: We compute the similarity between users based on these latent features. This allows us to identify users who have similar tastes in movies.

Similar User Recommendations: Once we have identified similar users, we can recommend movies that these similar users have liked.

# 5. Examples of Use
Content-Based Filtering Example: Given a movie title, the system recommends a list of similar movies based on the movie title alone.
Collaborative Filtering Example: Given a user ID, the system finds similar users and suggests movies that these users have rated highly.
Conclusion
This project demonstrates how different recommendation algorithms can be implemented using Python and various machine learning techniques. The content-based method is useful when you have detailed item information (e.g., movie titles), while collaborative filtering excels when you have user interaction data (e.g., user ratings).
