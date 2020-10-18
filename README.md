#      Toxic Text Classification Approach 

 

In my approach towards toxic text classifier, I first inspected my dataset and came to know about multilabel classification. It assigns to each sample a set of target labels. This can be thought as predicting properties of a data-point that are not mutually exclusive. 

 

STEP 1:- PREPROCESSING 

Data Cleaning 

The data used consist of many Wikipedia comments which have been labelled by humans according to their relative toxicity. 

The data includes the following: 

train.csv: the training set, contains comments with their binary labels. 

test.csv: the test set, predict toxicity probabilities for these comments. 

sample_submission.csv: the submission sample with the correct format 

In my approach I will first do data cleaning and then check for any ambiguity in the dataset. 

 

Data Analysis 

The approach we are taking is to feed the comments into the LSTM as part of the neural network but we can’t just feed the words as it is, so we performed tokenization and did index representation. We used word cloud to find the intensity of different toxic comments in various categories of the dataset. 

 

Step 2:- Embeddings 

 

The data representation normally used on our vocabulary is the one-hot encoding where every word is transformed into a vector with a 1 corresponding it its location. 

We have hence taken the approach of using a Word2Vec technique to find continuous embeddings for our words. 

 

Step 3:- MACHINE LEARNING MODELS 

Naive bayes,svm,logistic regression 

TF-IDF is short for term frequency-inverse document frequency which is a method to display how important a word is to a document in a corpus. The tf–idf value increases proportionally to the number of times a word appears in the document and is offset by the number of documents in the corpus that contain the word, which helps to adjust for the fact that some words appear more frequently in general. 

 

Convolution Neural Network (CNN with word embedding) 

The CNN model we will be using consists of one 1-dimensional convolutional layer across the concatenated word embeddings for each input comment. The convolutional layer has 128 filters with a kernel size of 5 so that each convolution will consider a window of 5 word embeddings. The next layer is a fully connected layer with 50 units which is then followed by the output layer. 

Recurrent Neural Network (RNN) with Long Short Term Memory (LSTM) cells 

The RNN type model used here is the LSTM model. This model is attractive because the individual cell states in the model have the ability to remove or add information to the cell state through gates layers. This is useful in practice because it allows the model to remember insights derived from words throughout the comment. The LSTM model consist of one densely connected layer with 60 units across the concatenated word vectors for each of the words in the comment. 

 

 

 

 

PREPARED BY:- 

Divyansh Singhal 

(ML INTERN Team 8) 

 
