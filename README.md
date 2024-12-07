# Stock Movement Prediction Project

This project demonstrates how to scrape data from Telegram, preprocess it, and train a machine learning model to predict stock movements.

## Project Overview
The goal of this project is to scrape stock market-related discussions from Telegram channels, preprocess the data, analyze the sentiment, and then train a machine learning model to predict stock movements (e.g., "up", "down", or "neutral"). The workflow consists of the following stages:
1. **Data Scraping**: The `data_scraping.ipynb` notebook scrapes data from stock-related Telegram channels.
2. **Data Preprocessing and Model Training**: The `Data_Preprocessing_and_Prediction_Model.ipynb` notebook processes the scraped data and trains a prediction model using Random Forest.

## Installation
1. Clone the repository: git clone https://github.com/your-username/stock-movement-prediction.git

2. Navigate to the project directory: cd stock-prediction

3. Create a virtual environment (optional but recommended): python -m venv venv

4. Activate the virtual environment: venv\Scripts\activate

## Dependencies
To run this project, you'll need the following Python packages:

- pandas
- scikit-learn
- beautifulsoup4
- requests
- telethon
- nltk
- matplotlib
- nest_asyncio
- csv
- 
You can install these dependencies by running:
pip install -r requirements.txt

## Running the Code
Step 1 : Scraping Data
Run the 'data_scraping.ipynb' notebook to scrape data from the selected Telegram channels.

Step 2 : Preprocessing and Model Training
Once the data is scraped, run the 'Data_Preprocessing_and_Prediction_Model.ipynb' notebook to preprocess the data, train the model, and evaluate its performance.

## Results
The model achieves a classification accuracy of 100% on the test data.

## Challenges
During the development of this project, I encountered several challenges and resolved them as follows:

- Data Scraping Challenges:
  API Limitations: While scraping data from Telegram, I faced limitations on the number of requests that could be made in a short period. To mitigate this, I implemented a batching mechanism where requests were made in batches, with pauses in between, to stay within the rate limits.

- Data Preprocessing:
  Handling Missing Data: During preprocessing, I had to handle missing or incomplete data in the dataset. I used techniques like imputation and data cleaning to ensure the model had valid inputs for training.

- Model Performance:
  Imbalanced Classes: The dataset had imbalanced classes (more neutral than other classes), which affected the performance of the model. I used oversampling techniques (like Random Sampling) to balance the dataset and improve model performance.

## Future Improvements
Here are some potential future improvements for the project:

1. Integrate Multiple Data Sources:
   In addition to Telegram, data can be scraped from other social media platforms like Twitter or Reddit to create a more robust prediction model.
2. Improve Prediction Accuracy:
   Implement more advanced NLP techniques like word embeddings (e.g., Word2Vec, GloVe) and try different machine learning algorithms to improve model performance.
3. Real-Time Predictions:
   Develop a system that can predict stock movements in real-time as new data arrives from the scraped sources.