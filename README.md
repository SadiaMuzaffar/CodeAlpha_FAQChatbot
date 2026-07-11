# FAQ Chatbot 

A chatbot that answers user questions by matching them to the most 
similar question in an FAQ dataset using NLP techniques.

## How it works
1. Text preprocessing: lowercase, remove punctuation, remove stopwords (NLTK)
2. TF-IDF vectorization to convert text into numeric vectors
3. Cosine similarity to find the closest matching FAQ
4. Returns the matched answer if similarity score > 0.3, else returns 
   a fallback message

## Dataset
Ecommerce FAQ Chatbot Dataset (79 Q&A pairs) — sourced from Kaggle

## Tools used
Python, NLTK, scikit-learn (TF-IDF, cosine similarity), pandas

## Limitations
- Matches based on word overlap, not meaning — so synonyms 
  (e.g. "refund" vs "return", "sign up" vs "create account") 
  are not always recognized
- Can occasionally match on a shared but contextually different 
  word (e.g. "card details" vs "gift card")
- Future improvement: use word embeddings or sentence transformers 
  for semantic matching

## How to run
Open `FAQ_Chatbot.ipynb` in Google Colab, upload the dataset file, 
and run all cells.
