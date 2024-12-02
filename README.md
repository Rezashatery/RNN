# RNN and Transformers for Subjectivity Classification

This project explores the use of Recurrent Neural Networks (RNNs) and Transformers for classifying the subjectivity of Italian sentences. 

## Problem Description

The goal is to build a model that can predict whether a given sentence is subjective or objective. The dataset used is a collection of Italian newspaper articles labeled as Objective or Subjective. Each article is divided into sentences, which are consequently classified as either Subjective or Objective. The dataset can be found [here](https://github.com/francescoantici/SubjectivITA).

## Approach

Two main approaches are explored:

1. **RNNs**:  LSTM and Bidirectional LSTM models are implemented and evaluated.
2. **Transformers**: A pre-trained BERT model (AlBERTo) is fine-tuned for the task.

## Data

The dataset is split into train, validation, and test sets. The sentences are tokenized and padded to a fixed length. For the Transformer model, the data is preprocessed using the `AutoTokenizer` from the `transformers` library.

## Models

### RNN

* A basic LSTM model is implemented using `keras.layers.LSTM`.
* A Bidirectional LSTM model is implemented using `keras.layers.Bidirectional`.

### Transformer

* A pre-trained AlBERTo model is fine-tuned for the task using the `transformers` library.

## Evaluation

The models are evaluated using the `classification_report` function from `sklearn.metrics`. The report provides precision, recall, F1-score, and support for each class (Objective and Subjective).

## Usage

1. **Data**: Download the train, validation, and test files from the [repository](https://github.com/francescoantici/SubjectivITA/tree/main/datasets/sentences).
2. **Dependencies**: Install the necessary libraries:
3. bash !pip3 install tensorflow transformers scikit-learn pandas numpy

4. 3. **Run the notebook**: Execute the cells in the notebook to train and evaluate the models.


## Results

The results of the models are presented in the notebook. The Transformer model generally achieves better performance compared to the RNN models.

## Conclusion

This project demonstrates the effectiveness of RNNs and Transformers for subjectivity classification. The pre-trained AlBERTo model shows promising results and highlights the benefits of using pre-trained language models for NLP tasks.
