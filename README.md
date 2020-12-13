# Att-BiLSTM Model for Tweet Emotion Recognition
An attention based Bi-LSTM model for tweet emotion recognition.

## Requirements
The model uses pre trained GloVe vectors which can be found at https://nlp.stanford.edu/projects/glove/
We use 50 dimensions of vectors particularly trained on twitter data. 

## Preprocessing
The data found in the file tweet_emotion.csv and the preprocessing and combining of the data is implemented in the preprocess.ipynb notebook.

## Attention based Bidirectional LSTM Model
The basic idea is to implement an LSTM layer with an attention layer on top to include output of all the LSTM cells instead of basing on just the output of the last cell in the layer. The attention layer merges each word level output to create a sentence level feature to capture the global information of the sentence to be considered for the classification.


