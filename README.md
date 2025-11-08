# Mini AI based on sentiment analysis for movie raccomandations

Based on Node.js (backend)
Using The Movie Database (API key to get movie library)
Cloud ML model invocations with AWS Bedrock

First: We define basic search parameters (e.g., 2024 releases, popular genres).

/recommend Route: This endpoint is our main action handler 

fetchMovies(prefs): It hits the TMDB API to get 10 movies based on the user's preferences.

explainChoices(movies, prefs): This sends the list of 10 movies and the user's specific text query to the Bedrock LLM.

LLM Task: The LLM reads the 10 movies, selects the best 3, and writes a fun, critical summary explaining why those 3 are perfect choices.

Response 200 OK: The server sends the LLM's structured JSON response back.

We will use Postman VScode extension for endpoint testing
