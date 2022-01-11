# Sentiment analysis with TF-IDF & BERT

Online store starts new service allows users to edit and add item's description like it does in wiki community. It need to be developed the tool to find toxic comments and send them to moderation. Our goal is to build model that predicts whethere comment toxic or not. We're going to use Logistic Regression as a model and two methods to vectorize features - TF-IDF and BERT. Let's see which one will show better results! <br />
Also we implement fine-tuning BERT models. And it appears that their perfomances exceed are expectations! 

```
              precision    recall  f1-score   support

           1       0.90      1.00      0.95       180
           0       0.00      0.00      0.00        20

    accuracy                           0.90       200
   macro avg       0.45      0.50      0.47       200
weighted avg       0.81      0.90      0.85       200
```

## Usage
First of all you should install transformers, nltk and contractions

```
!pip install transformers
!pip install nltk
!pip install contractions
pip install ktrain
!pip install transformers
```

## Requirements
python 3 <br />
Also you'll need a GPU to make embeddings more faster ;)
