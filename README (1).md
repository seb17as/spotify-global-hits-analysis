# Spotify Global Hits Analysis

Exploratory data analysis and machine learning classification of global Spotify chart data across 73 countries, examining how audio features relate to streaming popularity, regional listening preferences, and global hit prediction.

## Dataset

**Source:** [Top Spotify Songs in 73 Countries (Daily Updated)](https://www.kaggle.com/datasets/asaniczka/top-spotify-songs-in-73-countries-daily-updated) via Kaggle API

The dataset contains daily Top 200 charts from 73 countries with audio features (energy, danceability, valence, tempo, acousticness, instrumentalness, liveness, loudness, speechiness) and streaming metrics.

## Research Questions

1. **Audio Features vs. Popularity** — Which audio features correlate most strongly with streaming volume and global chart reach?
2. **What Makes a Top 10 Hit?** — Do Top 10 songs differ significantly in energy, danceability, and geographic reach compared to lower-charting tracks?
3. **Regional Listening Profiles** — How do average audio feature preferences vary across world regions (Latin America, Europe, Asia, North America, MENA)?
4. **Country Clustering** — Can unsupervised learning (K-Means) reveal natural groupings of countries based on listening preferences?
5. **Global Hit Prediction** — Can audio features alone predict whether a song will chart in 10+ countries? (Binary classification with Logistic Regression and Random Forest)
6. **Seasonal Trends** — How do listening patterns shift across seasons, holidays (Christmas, Valentine's Day), and summer months?

## Methods & Tools

| Category | Details |
|---|---|
| **Languages** | Python |
| **EDA & Visualization** | Pandas, Matplotlib, Seaborn |
| **Machine Learning** | Scikit-learn (Logistic Regression, Random Forest, K-Means, PCA) |
| **Feature Engineering** | Song-level aggregation, region mapping, seasonal flags, rank categorization |

## Key Findings

- **Loudness and energy** show the strongest positive correlations with streaming metrics among audio features.
- **Top 10 songs** exhibit higher energy and danceability compared to lower-charting tracks, and appear in significantly more countries.
- **K-Means clustering (k=4)** groups countries into distinct listening profile clusters that partially align with geographic regions — Latin American countries cluster tightly together, while European and Asian markets show more variation.
- **Random Forest outperforms Logistic Regression** for global hit classification, with loudness, tempo, and speechiness emerging as the most important predictive features.
- **Seasonal patterns** are observable: acousticness rises in December (driven by Christmas music), while danceability and valence peak during summer months.

## Project Structure

```
├── final.ipynb          # Complete analysis notebook
├── README.md            # Project documentation
└── .gitignore           # Excludes data files
```

## How to Run

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn kaggle
   ```
3. Configure your [Kaggle API credentials](https://www.kaggle.com/docs/api)
4. Run the notebook — the dataset downloads automatically via the Kaggle API

## Author

Sebastian — M.S. Data Science & AI, Florida International University
