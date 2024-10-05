# Sentiment Analysis of IMDB Movie Reviews

## Project Overview
This project focuses on sentiment analysis of movie reviews from the IMDB dataset. The model classifies movie reviews as either positive or negative, providing insights into audience feedback for movies. The task was implemented using an LSTM-based deep learning architecture to analyze the text data and predict sentiment.

## Dataset
The dataset used for this project contains 50,000 movie reviews from the IMDB website, available on Kaggle:(https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)

![image](https://github.com/user-attachments/assets/35785a1d-877f-46d2-a2fc-6029558e9495)

## Data Preprocessing
To prepare the dataset, the following preprocessing steps were applied:

* Converted all text to lowercase.
* Removed HTML tags from reviews.
* Filtered out non-alphabetic text.
* Removed common stop words to focus on key terms.
* Applied lemmatization to reduce words to their root forms.
* Tokenized the reviews and applied padding sequences to ensure uniform input length

  ![image](https://github.com/user-attachments/assets/69fdada7-8762-4aae-8007-51b495031aa1)

  - Achieved 87.26% accuracy on the test set
##Model Architecture
The sentiment classification model is built using an LSTM (Long Short-Term Memory) architecture, known for its effectiveness with sequential data like text. Key details of the model include:

* Embedding layer:Converts text input into dense vectors of fixed size.
* 2LSTM layers:Used to capture the sequence information from the revies.
* Dropout layers:Two dropout layers were added after each LSTM layer for regularization to prevent overfitting.
* Softmax layer:Outputs the probability distribution for positive and negative sentiment.

  ![image](https://github.com/user-attachments/assets/85293c29-0613-4df3-82f7-dec76cb8b8fb)


##Training
 * Epochs: 10
 * Batch Size: 32
 * Optimizer: Adam
 * Loss Function: Sparse categorical cross-entropy

Gradio Interface
To make the model more interactive, a Gradio GUI was developed. This allows users to input a movie review and receive the predicted sentiment in real time.

![image](https://github.com/user-attachments/assets/f6cff75a-dbd0-4023-b4ce-ead3e97103ba)

  
