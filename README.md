This project investigates whether early audience engagement signals predict a movie's long-term success (measured by IMDb vote count) better than traditional production-based features, using an integrated dataset of 36,188 movies built from IMDb, MovieLens, and TMDB.

Models Implemented

Baseline: Linear Regression (Combined features) with adjusted R² of 0.47
Primary: Random Forest Regression (Combined features) with R² of 0.86 and RMSE of 0.70

The Random Forest model substantially outperformed the linear baseline across all feature groups, confirming strong non-linear relationships between audience engagement and long-term popularity. Feature importance analysis showed MovieLens rating count as the dominant predictor, accounting for roughly 82% of total model importance.

Key Steps:
Data integration across three sources (IMDb, MovieLens, TMDB) using IMDb identifiers as the primary key, following the CRISP-DM framework. Data cleaning included removing invalid records, zero-vote movies, and runtime/release-year outliers. Feature engineering included log transformations (vote count, budget, rating count), movie age, release month, and genre-based features. Features were grouped into three sets — production-only, audience-only, and combined - and each was tested with both models (80/20 train-test split). Model evaluation used R² and RMSE, with feature importance extracted from the best Random Forest model.

Tech Stack: Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Linear Regression, Random Forest

Dataset: IMDb, MovieLens, and TMDB (integrated dataset of 36,188 movies) - link in project report (Google Drive)
