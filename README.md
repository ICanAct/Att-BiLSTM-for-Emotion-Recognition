# Att-BiLSTM Model for Tweet Emotion Recognition
An attention based Bi-LSTM model for tweet emotion recognition.

## Requirements
The model uses pre trained GloVe vectors which can be found at https://nlp.stanford.edu/projects/glove/
We use 50 dimensions of vectors particularly trained on twitter data. 

## Preprocessing
The data found in the file tweet_emotion.csv and the preprocessing and combining of the data is implemented in the preprocess.ipynb notebook.

## Attention based Bidirectional LSTM Model
The basic idea is to implement a Bi directional LSTM layer with an attention layer on top to include output of all the LSTM cells instead of basing on just the output of the last cell in the layer. The attention layer merges each word level output to create a sentence level feature to capture the global information of the sentence to be considered for the classification.
![Alt text](https://github.com/ICanAct/Att-BiLSTM-for-Emotion-Recognition/blob/screenshots/Screenshot%202020-11-21%20at%2011.31.36%20PM.png)

## Results
### Accuracy
![Alt text](https://github.com/ICanAct/Att-BiLSTM-for-Emotion-Recognition/blob/screenshots/Bilstm_accuracy%20(1).png)
### Classification Report
![Alt text](https://github.com/ICanAct/Att-BiLSTM-for-Emotion-Recognition/blob/screenshots/Screenshot%202020-12-14%20at%202.27.06%20AM.png)

we can see that the hate and anger tweets are classified with high precision. This might be due to the hate and anger tweets being very different and unambiguous compared to other tweets. The overall f1 scores are fairly decent for all the classes except the neutral class.

## References

[1] P. Zhou, W. Shi, J. Tian, Z. Qi, B. Li, H. Hao, and B. Xu, “Attention-Based Bidirectional Long Short-Term Memory Networks for Relation Classification,” Proceedings of the 54th Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers), 2016.
