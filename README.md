# Simple Spam Detector
This project is a simple but effective spam detector built with Python and scikit-learn. It uses natural language processing (NLP) techniques to preprocess text messages and a machine learning model to classify them as either "spam" or "ham" (not spam).

This is a great beginner project for anyone interested in AI, machine learning, and NLP.

## How it Works
The process can be broken down into a few key steps:

Data Loading: We start with a dataset of labeled text messages (spam or ham).

Text Preprocessing: This is a critical step to clean and prepare the text data for the model. The steps include:

Lowercasing: Converting all text to lowercase.

Tokenization: Splitting the text into individual words.

Removing Stop Words: Filtering out common words that don't add much meaning (e.g., "the", "a", "is").

Lemmatization: Reducing words to their base or root form (e.g., "running" becomes "run").

Feature Extraction (TF-IDF): The cleaned text is converted into numerical data that the machine learning model can understand using a technique called Term Frequency-Inverse Document Frequency (TF-IDF).

Model Training: A Logistic Regression classifier is trained on the preprocessed data.

Prediction: The trained model can then be used to predict whether a new, unseen text message is spam or not.

## How to Use
1. Clone the repository
git clone <your-repository-url>
cd <your-repository-folder>

2. Install Dependencies
It's recommended to use a virtual environment.

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

Then, install the required packages:

pip install -r requirements.txt

3. Download NLTK Data
The first time you run the script, it will require some data from the NLTK library. Run the following command in your terminal after activating your virtual environment:

python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords'); nltk.download('wordnet')"

4. Run the Spam Detector
You can run the script from your terminal:

python spam_detector.py

The script will train the model on the data.csv file and then classify a few example sentences, printing the results to the console. You can modify the spam_detector.py file to classify your own text files or sentences.
