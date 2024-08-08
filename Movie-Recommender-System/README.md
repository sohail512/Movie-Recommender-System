# Movie-Recommender-System

<b>Overview</b>

This project is a movie recommendation system developed using Python and Streamlit, hosted on Heroku. It leverages the TMDB (The Movie Database) API for fetching movie details and posters, and uses NLTK for text preprocessing. The recommendation algorithm is based on cosine similarity calculated from movie overviews, genres, keywords, cast, and crew.

<b>Features</b>

User-friendly interface developed using Streamlit
Dynamic fetching of movie posters from the TMDB API
Personalized movie recommendations based on content similarity
Deployed on Heroku for easy access and scalability

<b>Technologies & Algorithms</b>

Programming Languages: Python
Libraries and Tools: Streamlit, pandas, requests, pickle
Natural Language Processing: NLTK (tokenization, stemming, stop word removal)
Machine Learning: Cosine similarity
Deployment: Heroku

<b>Project Structure</b>

app.py: Main application file containing the Streamlit app code.
movie_dict.pkl: Pickled dictionary of movie data.
similarity.pkl: Pickled similarity matrix.
requirements.txt: List of required Python libraries.
tmdb_5000_movies.csv: Dataset containing movie information.
tmdb_5000_credits.csv: Dataset containing movie credits information.

<b>Installation</b>

1. Clone the repository: "https://github.com/sohail512/Movie-Recommender-System"
2. Navigate to the project directory: cd movie-recommendation-system
3. Extract the similarity.tar file: "tar -xzvf similarity.tar.gz"
4. Install the required dependencies: "pip install -r requirements.txt"
5. Create an tmdb api for movies on tmdb website to use it your code

<b>Usage</b>

1. Run the Streamlit application: "streamlit run app.py"
2. Open the provided URL in your browser to access the application.

<b>Data Preprocessing</b>

The movie data is preprocessed using the following steps:

- Tokenization of movie overviews, genres, keywords, cast, and crew.
- Removal of stop words and stemming using NLTK.
- Combining textual features into a single 'tags' column.
- Conversion of text data into vectors using CountVectorizer.
- Calculation of cosine similarity between movie vectors.

<b>Recommendation Algorithm</b>

The recommendation algorithm works as follows:

- Calculate the similarity of the selected movie to all other movies using cosine similarity.
- Sort the movies based on similarity scores.
- Recommend the top 5 most similar movies to the selected movie.

<b>API Integration</b>

The application fetches movie posters dynamically using the TMDB API:

- fetch_poster(movie_id): Function to fetch the movie poster URL based on the movie ID.

<b>Deployment</b>

The application is deployed on Heroku for easy access:

- Ensure all necessary files (app.py, requirements.txt, etc.) are included.
- Use Heroku CLI to deploy the application.

<b>Future Enhancements</b>

- Incorporate user feedback and ratings to improve recommendation accuracy.
- Explore additional recommendation algorithms such as collaborative filtering.
- Enhance the user interface with more interactive features.
