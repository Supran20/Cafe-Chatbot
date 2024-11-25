# Chitti Chatbot

Chitti is an AI-powered chatbot designed for easy interaction. It leverages Natural Language Processing (NLP) techniques to understand and respond to user queries in a conversational manner. This project demonstrates a simple chatbot system built using Python, PyTorch, and the Natural Language Toolkit (NLTK). The core functionality includes recognizing user input and responding with appropriate intent-based replies.

## Project Overview

- **nltk_utils.py**: Contains utility functions for processing text data (tokenization, stemming, and generating bag-of-words representation).
- **train.py**: Trains a neural network model on the processed data, using the intents defined in a JSON file, and saves the trained model.
- **model.py**: Defines a simple neural network architecture using PyTorch to classify user inputs into predefined intent categories.
- **chat.py**: Interacts with the trained model and uses it to classify user inputs in real-time, responding according to the identified intent.

## Files Overview

### nltk_utils.py

- **tokenize(sentence)**: Tokenizes the input sentence into words using NLTK.
- **stem(word)**: Applies stemming to reduce words to their root form.
- **bag_of_words(tokenized_sentence, all_words)**: Converts a sentence into a vector representation based on the presence of predefined words in `all_words`.

### train.py

- Loads intents from a JSON file.
- Preprocesses the data by tokenizing and stemming each word.
- Generates a bag-of-words representation for each input sentence.
- Creates a training dataset and trains a neural network using PyTorch.
- Saves the trained model parameters to a file (`data.pth`).

### model.py

- Defines a neural network architecture for text classification using PyTorch.
- The model consists of three fully connected layers with ReLU activation functions between them.

### chat.py

- Loads the trained model and intents.
- Accepts user input, processes it, and uses the model to predict the intent.
- Responds with a randomly selected response from the corresponding intent or states that it does not understand if the confidence is low.

## Prerequisites

- Python 3.x
- PyTorch
- NLTK

You can install the required dependencies using the following command:

```bash
pip install torch nltk
```
