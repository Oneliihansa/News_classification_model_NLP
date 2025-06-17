
## Project Overview

This project focuses on building a high-performing news article classifier using modern Natural Language Processing (NLP) techniques and a transformer-based deep learning model. The objective was to classify articles into one of five categories: Business, Opinion, Political Gossip, Sports, and World News using a real-world dataset.
## Dataset and Preprocessing

The dataset was compiled from Daily Mirror articles, available as separate Excel files for each category. These were merged into one comprehensive dataset. Extensive preprocessing steps were applied:

Punctuation and special characters were removed.

Stopwords were filtered out.

The top 30 most frequent and 100 rarest words were excluded to eliminate noise and outliers.

Tokenization was performed using NLTK.

Lemmatization was done using WordNet with Part-of-Speech (POS) tagging to preserve word meanings.

These steps helped in cleaning and normalizing the text data, making it suitable for model training.
##  Exploratory Data Analysis (EDA)

Before modeling, EDA was carried out to understand word distribution and category-specific patterns:

Word clouds were generated for each category to visualize dominant terms.

Bigrams and trigrams were extracted and visualized using bar plots.

A term frequency heatmap compared word importance across all categories.

Individual bar plots showed top keywords per category.
## Model Selection and Training

We chose the distilbert-base-uncased model from Hugging Face due to its excellent balance of speed and accuracy. DistilBERT retains 97% of BERT’s performance while being 60% smaller and faster, making it ideal for deployment.

Key Training Features:
-Stratified splitting of the dataset to preserve class balance in train/test sets.

-Learning rate warm-up (500 steps) to stabilize initial training.

-L2 regularization (weight decay) to reduce overfitting.

-Early stopping to prevent degradation in validation performance.

Training was done using Hugging Face's Trainer API with logging and evaluation at each epoch.


## Model Performance

The model achieved impressive results:

Accuracy: 92.63%

F1 Score (macro): 91.77%

These metrics demonstrate strong model performance and generalization across all five news categories.
## Deployment

To deploy this project run

https://huggingface.co/spaces/Oneli/News_Classification

A live inference demo was deployed on Hugging Face Spaces, allowing real-time classification of user-inputted news text. 

## Screenshots

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

