# Automated Sentiment Analysis for IMDB Dataset
## Project Overview
This project aims to develop an efficient automated machine learning (AutoML) framework for sentiment analysis on the IMDB movie review dataset. Sentiment analysis is a crucial task in natural language processing, with applications in areas like market research, customer feedback analysis, and social media analysis. The goal of this project is to build a robust and scalable pipeline that can effectively classify the sentiment (positive or negative) of textual data from the IMDB dataset.

## Dataset
The IMDB dataset is a widely recognized benchmark for sentiment analysis, consisting of a large collection of movie reviews labeled with positive or negative sentiments. The dataset poses interesting challenges due to the nuances of language used in the reviews.

## Pipeline Steps
- Data Preprocessing: The raw text data is transformed into a format amenable to machine learning models. This includes tokenization, removal of stop words, and vectorization using TF-IDF.
- Feature Engineering: Additional features may be extracted from the text data to improve the model's performance.
- Model Training: Two models are trained and evaluated: a baseline logistic regression model and a fine-tuned BERT (Bidirectional Encoder Representations from Transformers) model.
- Model Evaluation: The trained models are evaluated using standard metrics such as accuracy, precision, recall, and F1 score.
- Model Deployment: The best-performing model is packaged and deployed as a Flask API, containerized using Docker for scalability and reproducibility.
  
## Setup Instructions
Clone the repository: git clone https://github.com/your-username/automated-sentiment-analysis.git
Create a virtual environment and activate it.
Install the required dependencies: pip install -r requirements.txt
Run the Flask API locally: python app.py

## Folder structure:
Folder structure:
ml_pipeline   
|_ data : this folder contains the data needed to train/predict   
|_ documentations : this folder contains the documentation related to the pipeline design   
|_ models : this folder consists the trained model pipeline to be used in production(old version and new version of the model pipeline shall be stored here)       
   |_ requirements.txt : to be used to install the required packages to run the machine learning pipeline       
   |_ ML_full_pipeline.ipynb : the jupyter notebook file consisting of the full machine learning pipeline

## Usage
The deployed Flask API can be used to classify the sentiment of input text. To use the API, send a POST request to the /predict endpoint with the text data in the request body.

Example:
curl -X POST -H "Content-Type: application/json" -d '{"text": "This movie was amazing!"}' http://localhost:5000/predict
The API will respond with the predicted sentiment (either "positive" or "negative").

## Contribution Guidelines
Contributions to this project are welcome. If you would like to contribute, please follow these guidelines:

Fork the repository.
Create a new branch for your changes.
Make your changes and ensure that the code passes all tests.
Submit a pull request with a detailed description of your changes.
License
This project is licensed under the MIT License.


## Final Working Product:
![WhatsApp Image 2024-05-31 at 7 40 05 PM](https://github.com/hbsedki/MovieSentimentAnalysis/assets/150509637/92a4efb6-1f32-4e01-bdbf-a314addc6f94)

