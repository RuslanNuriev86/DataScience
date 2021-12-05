# Sentiment analysis with TF-IDF & BERT

Online store starts new service allows users to edit and add item's description like it does in wiki community. It need to be developed the tool to find toxic comments and send them to moderation. Our goal is to build model that predicts whethere comment toxic or not. We're going to use Logistic Regression as a model and two methods to vectorize features - TF-IDF and BERT. Let's see which one will show better results!

## Usage
First of all you should install transformers, nltk and contractions

```
!pip install transformers
!pip install nltk
!pip install contractions
```

## Requirements
python 3
Also you'll need GPU to make embeddings more faster ;)
