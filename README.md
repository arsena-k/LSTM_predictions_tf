# LSTM_predictions_tf
Use LSTM in tensorflow to predict outcomes from text data


**The goal** of these models was to train an LSTM network (long short term memory network, an artificial netural network architecture) predict depression labels (based on the PHQ-8) from transcribed verbal data. Data comes from from interivews with around 700 participants; these interviews were intended to simulate a structured psychiatric interview. 

Prediction options include: depression level (continuous, low/med/high, or binary), level for each of 8 possible depression symptoms based on PHQ-8 (low/med/high, or binary). You may need to change the cost function in the code depending on the outcome chosen. Depression data is often unbalanced (more lower levels of depression), so options in code for 1) undersampling the majority class (lower levels of depression) and 2) cost-senstive learning. For regularization, there are various options for dropout and L1/L2 regaularization. 

**Three variants of the model include in this repo:**

*1. RNN_PredictingPHQsymptoms_7.25_not_dynamic-multi_task-cleaned.8.22.ipynb*
* Embeddings learned along the way to replace uttered words with embeddings and then feed these into LSTM layer
* Options to predict multiple outcomes (e.g., jointly predict two specific depression symptoms) which could improve generalizability of the model

*2. RNN_PredictingPHQsymptoms_7.25_Undersampling,L2,Dropout-not_dynamic-embeddings_pretrained_.ipynb*
* Pre-trained embeddings from Word2Vec loaded in, these embeddings replace uttered words and then are fed into the LSTM layer

*3. RNN_PredictingPHQsymptoms_7.28_LIWC-Regression_denselayer.ipynb*
* Embeddings learned along the way to replaced uttered words with embeddings and then feed these into LSTM layer
* Predicts depression from utterances using a concatenation of: the utternace where words are learned as embeddings, and linguistic features of the utterances (derived from LIWC, ahead of time)

**Notes:** 
* This repository is intended to keep (unpolished) examples for building an LSTM in Tensorflow to predict outcomes from text data, rather than present any polished code or application
* Written in Python 2 with Tensorflow


