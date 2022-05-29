# News-Headlines-Dataset-For-Sarcasm-Detection

## Project Motivation

Sarcasm Detection mostly make use of Twitter datasets collected using hashtag based supervision

## File Descriptions
## Data
Each record consists of three attributes:

* ```is_sarcastic```: 1 if the record is sarcastic otherwise 0

* ```headline```: the headline of the news article

* ```article_link```: link to the original news article. Useful in collecting supplementary data


#### Notebooks

-The folder NOTEBOOKS contains many notebooks.

One notebook file 1) Preprocessing.ipynb which contains the loading and preprocessing the data code.
One notebook file 2) Feature_extraction.ipynb which contains the feature extraction code.
One notebook file 3) BOW Modeling.ipynb which contains the modeling code for the bag of word vectorization algorithm.
One notebook file 3) TF-IDF Modeling.ipynb which contains the modeling code for the TFIDF vectorization algorithm.


### Steps to build the model:

###### 1) Data Exploration and Text Processing
Common issues that we generally face during the data preparation phase:

1) too many spelling mistakes in the text.
2) too many numbers and punctuations.
3) too many emojis and emoticons and username and links too.
4) Some of the text parts are not in the English language. Data is having a mixture of more than one language.
4) Some of the words are combined with the hyphen or data having contractions word or Repetitions of words.


Here i will clean the text by doing the following steps:

1) Lowecasing the data.
2) Removing Puncuatations.
3) Removing Numbers.
4) Removing extra space.
5) Removing Contractions.
6) Removing HTML tags.
7) Removing & Finding URL and Email id.
8) Removing Stop Words
9) Removing Extra-spaces
10) Stemming
11) Spell Correction


###### 2) Feature Extraction

We cannot work on texts directly when using machine learning algorithms.So, we need to convert the text to numbers.

1) I used CountVectorizer feature extraction algorithm. 

2) I used TF-IDF feature extraction algorithm. 
Term Frequency (TF): Frequency of a term appearing in one document
Inverse Document Frequency (IDF): TFrequency of a term appearing a lot across documents.
TF-IDF are word frequency scores that try to highlight words that are more interesting.

The vectorized data is included in VECTORS file.


###### 3) Modeling
In this project, I used Support vector machine (SVM) and Multinomial Naive bayes Algorithms to classify the articles.

The best trained model is saved in MODELS file.


###### Metrics 
1) Accuracy

2) Confusion Matrix

3) Classification Report

## Acknowledgements
This dataset was collected from [TheOnion](https://theonion.com) and [HuffPost](https://www.huffingtonpost.com/).

## Cite
```
@article{misra2019sarcasm,
  title={Sarcasm Detection using Hybrid Neural Network},
  author={Misra, Rishabh and Arora, Prahal},
  journal={arXiv preprint arXiv:1908.07414},
  year={2019}
}

@book{book,
author = {Misra, Rishabh and Grover, Jigyasa},
year = {2021},
month = {01},
pages = {},
title = {Sculpting Data for ML: The first act of Machine Learning},
isbn = {978-0-578-83125-1}
}
```

