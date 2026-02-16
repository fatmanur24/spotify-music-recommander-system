# Spotify Music Recommender System

A simple music recommendation app. The `app.py` script uses a local CSV dataset (`music_data.csv`) and
a precomputed similarity matrix (`similarity.npy`) to recommend songs similar to a selected track. Album
artwork for each recommendation is fetched from the Spotify Web API.

**Features**
- Dropdown to select a song
- Fetch album artwork using the Spotify API
- Display recommendations based on a precomputed similarity matrix

**Requirements**
- Python 3.8+
- The following Python packages: `streamlit`, `spotipy`, `pandas`, `numpy`

Install the dependencies with:

```bash
pip install streamlit spotipy pandas numpy
```

**Required files**
- `app.py` — main application script
- `music_data.csv` — song dataset (should include at least `song` and `artist` columns)
- `similarity.npy` — precomputed similarity matrix (NumPy format)

Note: `CLIENT_ID` and `CLIENT_SECRET` are currently set directly in `app.py`.
For security, it is recommended to store these credentials as environment variables or in a
configuration file instead of hardcoding them.

How to get Spotify credentials and run the app:

1. Create an app at https://developer.spotify.com and obtain `CLIENT_ID` and `CLIENT_SECRET`.
2. Place `music_data.csv` and `similarity.npy` in the project root.

Run the application:

```bash
streamlit run app.py
```

In the opened browser page select a song and click the `Show Recommendation` button to view suggestions.

If you want, I can also add instructions for how to generate `similarity.npy`, provide an example
`music_data.csv` format, or create a `requirements.txt` file — tell me which you'd like.

<img width="1892" height="830" alt="image" src="https://github.com/user-attachments/assets/93b0f3d1-7848-4d0d-944e-7df6fce5ef7a" />
