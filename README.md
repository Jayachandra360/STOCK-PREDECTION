# Q-Learning Stock Prediction

## Overview
This project implements a Q-learning based stock prediction system that utilizes reinforcement learning techniques to make buy, sell, or hold decisions for a given stock symbol. It incorporates real-time data fetching, technical indicator calculation, sentiment analysis on news articles, and machine learning models for prediction.

## Features
- Fetches real-time stock data using Yahoo Finance API.
- Calculates various technical indicators such as SMA, EMA, RSI, Bollinger Bands, VWAP, and CMF.
- Utilizes sentiment analysis on news articles related to the stock symbol to determine market sentiment.
- Implements a Q-learning algorithm for reinforcement learning to predict optimal actions (BUY, SELL, HOLD) based on the current state.
- Trains and updates Q-values during market hours, considering both price movements and sentiment scores.
- Uses a Random Forest classifier for training the model and LSTM neural networks for deep learning-based predictions.
- Provides visualization of model performance using confusion matrices.

## Setup Instructions
1. Clone the repository to your local machine:

    ```
    git clone <repository_url>
    ```

2. Install the required Python packages using pip:

    ```
    pip install -r requirements.txt
    ```

3. Make sure you have the necessary API keys (e.g., News API) and update them in the code where required.

4. Run the main script to start the prediction process:

    ```
    python main.py
    ```

## File Structure
- `main.py`: Main script to run the stock prediction system.
- `q_learning.py`: Implementation of the Q-learning algorithm and reinforcement learning components.
- `utils.py`: Utility functions for data preprocessing, model training, and sentiment analysis.
- `requirements.txt`: File containing the required Python packages and their versions.

## Usage
- Ensure that the system is running during market hours for real-time predictions.
- Monitor the model performance through the generated confusion matrices.
- Adjust hyperparameters and thresholds as needed for improved prediction accuracy.


## Acknowledgments
- This project was inspired by the work of [authors/contributors], and we acknowledge their contributions to the field of stock prediction and reinforcement learning.

---

Feel free to customize the README file with additional information specific to your project or any acknowledgments you'd like to include.

Summary of code:
The provided code implements a Q-learning-based stock prediction system using reinforcement learning techniques. Here's a summary of its key components and functionalities:

1. **QLearningStockPrediction Class**: This class encapsulates the Q-learning algorithm. It includes methods for initializing Q-values, choosing actions, updating Q-values, saving/loading Q-values, and making predictions.

2. **fetch_data Function**: Fetches historical stock price data using the Yahoo Finance API.

3. **add_technical_indicators Function**: Calculates various technical indicators (e.g., SMA, EMA, RSI, Bollinger Bands, VWAP, CMF) from the stock price data.

4. **preprocess_data Function**: Prepares the data by adding technical indicators and handling missing values.

5. **calculate_reward Function**: Computes the reward based on the action taken and the change in stock price.

6. **build_model Function**: Constructs a deep learning model (LSTM) for stock prediction.

7. **fetch_news_sentiment Function**: Retrieves sentiment scores from news articles related to the stock symbol using a hypothetical API (e.g., News API).

8. **plot_confusion_matrix Function**: Visualizes the confusion matrix to evaluate model performance.

9. **calculate_reward_based_on_sentiment Function**: Assigns rewards based on sentiment polarity of news articles.

10. **is_usa_market_open Function**: Checks if the USA stock market is open based on current time.

11. **main Function**: Implements the main logic for training and making predictions during market hours. It continuously fetches real-time data, updates Q-values, and makes predictions using the Q-learning algorithm.

12. **README File**: Provides instructions for setting up the project, running the code, and using the system. It also includes an overview, features, file structure, usage guidelines, license information, and acknowledgments.

Overall, the code aims to predict optimal actions (BUY, SELL, HOLD) for a given stock symbol by learning from historical data, technical indicators, and sentiment analysis of news articles. The Q-learning algorithm is continuously trained and updated during market hours to adapt to changing market conditions.
