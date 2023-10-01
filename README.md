# FAQ-Voicebot-with-Neural-Intent-Identification
The FAQ Voicebot with Neural Intent Identification - Pizza Ordering is a conversational AI system that helps customers place pizza orders using voice commands.The system is built using a neural network-based intent identification model that is trained on a dataset of pizza ordering FAQs. The interface is integrated with a text-to-speech (TTS) engine, which converts the system's responses into natural-sounding speech.This reduces the need for manual input and enhances the customer experience.

Skills & Tools Covered: Text-to-Speech (TTS), Conversational AI, Voicebot, Natural Language Processing (NLP), Intent Identification, Neural Networks, RNN, LSTM.

Observations and Conclusions:
- I have created a FAQ bot for a pizza company.
- The model is fed with a list of 21 intents, each with possible responses.
- The model is expected to predict an appropriate response for an user input, which is then converted into text-to-speech format.
- I experimented with two different models (i) ANN and (ii) LSTM.
- None of the models performed very well with the validation set, although they fitted the training set well.
- ANN model performed better with both training set and validation set accuracies of responses as compared to the LSTM. This is possibly because of the following reasons:

- The training data is small. This may not be enough for the LSTM model to capture the context of the user input. To mitigate this, we must increase the input data. However, we are also limited by the fact that this is a FAQ bot and there are only limited, fixed set of questions and answers that can be asked and answered. Hence, there is not much variation in the input data for LSTM model to learn from.
- ANN, on the other hand fits the limited input data well and performs better on the training data and reaches a 100% accuracy rate with the prediciton with training set in 28 epochs.
- Given a data set, there is no fixed answer as to which architecture will perform better. However, increasing the amount of input data should definitely improve the results in LSTM model.

- I have also tweaked with the architectures in both models. I simplified the models so they do not overfit the the training set. Overfitting the training set means the model has memorized the pecularities and noises embedded in the specific training set and will perform badly with validation and test sets. Using drop layer worsended the training data accuracy. I have also used decay factor for the learning rate to automatize the tuning of the hyperparameter.
