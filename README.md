Game Playing Strength Prediction using MCTS Variants 🧠

This repository contains the solution for a Kaggle competition focused on predicting the strength of Monte-Carlo Tree Search (MCTS) agents in board games. The objective is to predict the advantage of the first agent over the second based on various game configurations and agent performance metrics.
Key Features:

    Data Preprocessing:
        Handles missing values and transforms categorical features into numerical ones.
        Drops columns that are entirely NaN and scales numeric features using StandardScaler.

    Model Training:
        Utilizes a RandomForestRegressor model with hyperparameter tuning.
        Splits data into training and validation sets to ensure model robustness.
        Metrics used for evaluation: Mean Absolute Error (MAE), Root Mean Squared Log Error (RMSLE), and R² score.

    Test Data Handling:
        Automatically fills missing values for key features (num_wins_agent1, num_draws_agent1, and num_losses_agent1) using the median values from the training data.
        Applies the same preprocessing pipeline as the training data.

    Prediction and Submission:
        Generates predictions on the test data, clipping them between -1 and 1 to meet competition requirements.
        Outputs predictions to a CSV file for submission.

Dependencies:

    Python
    NumPy
    Pandas
    Polars
    Scikit-learn

Project Structure:

    train.csv, test.csv, concepts.csv: Datasets used for training, testing, and understanding the game setup.
    sample_submission.csv: Template for submitting predictions to the competition.
    model.py: Contains the model training, evaluation, and prediction logic.
