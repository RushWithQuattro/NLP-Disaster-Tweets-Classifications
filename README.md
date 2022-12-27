# NLP-Disaster-Tweets-Classifications

This project aims to practice using python to implement some famous NLP models to classify tweets that are about real natural
disasters versus those that are not. Training and testing datasets are provided by Kaggle.com.
Training and testing data provided by Kaggle.com Competition: "Natural Language Processing with Disaster Tweets"
https://www.kaggle.com/c/nlp-getting-started/data. 
The dataset contains text-based, unequal length tweets about natrual disasters. The
training set consists of tweets and lablels( two classes 0,1, indicating if that tweet is about a real diaster or not).
 3 deep learning models were chosen for this natural language classfication problems:
1. Single dense layer model;
2. Transfer learning: Single dense layer model with pretained text embedding layer;
3. Transfer learning: 1-dimensional CNN model with pretrained text embedding layer.
For pre-trained encoder, we choose the Universial Sentence Encoder (USE) as our pretrain text embedder.
We compare the performance between these models in terms of training time, prediction accuracy, etc.

In our main program, we created 3 classes:
1. Model_Servicing Class: this class aim to provide a range of "services" for a deep leaning model created from the TensorFlow
Framework. Specifically, it wraps a user constructed model as its class attributes, and allows easy model compilation, training, making
predictions, and returning evaluation matrics.
2. NLP_Model-Servicing Class: subclass of Model_Servicing. It inherents from the Model Servicing class, and is customized spacifically
for Natrual Language Classification models. (For example, model evaluation in this class implements confusion matrix to produce a list
of commonly used matrices for classfication problems; Model compilation utilized binary crossentropy loss function)
3. Dset Class: A class that helps cleaning and managing training and testing dataset.

Main() function
In main() function, we constructed 3 deep-learning models for disaster tweets classfications. A simple, single dense layer model; A
single dense layer model with pretained text embedding layer; A 1-dimensional CNN model with pretrained text embedding layer. Then,
we initilize 3 instances of the NPL_Model_Servicing class to take care of the compilation, training, and evaluation of the 3 models.
