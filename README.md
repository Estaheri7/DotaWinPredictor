# Dota 2 Match Outcome Prediction

## Overview

This project aims to predict the outcome of [Dota 2](https://www.dota2.com/home) matches based on the heroes picked by both the Radiant and Dire teams. Using machine learning techniques, we train a model to determine the likelihood of either team winning given the heroes selected during the drafting phase.

## Project Structure

- **Data Collection**: We collect match data, including the heroes picked by both teams and the match outcome, using the [OpenDota API](https://docs.opendota.com).
- **Data Preprocessing**: The hero IDs for both teams are encoded using one-hot encoding to create a feature set for machine learning models.
- **Model Training**: A machine learning model is trained on the preprocessed data to predict the match outcome.
- **Prediction**: The trained model is used to predict the outcome of new matches based on the heroes picked.

## Data Directory
  
- **data/**
  - `matches.csv`: Collected match data including match IDs, hero picks, and match outcomes.
  - `heroes.csv`: List of Dota 2 heroes with their corresponding IDs.

## Notes

- The OpenDota API may return the same match details if queried too frequently. It is recommended to space out API requests to avoid collecting duplicate data.
- The model's performance may vary depending on the amount and quality of data collected. Experimenting with different machine learning algorithms and hyperparameters is encouraged.

## Future Work

- **Feature Engineering**: Explore additional features such as player rankings, hero synergy, and counter-picks to improve model accuracy.
- **Model Optimization**: Experiment with different machine learning algorithms and techniques like cross-validation, hyperparameter tuning, and ensemble methods.
- **Real-time Prediction**: Integrate the model with live match data to provide real-time win probability predictions during ongoing matches.
