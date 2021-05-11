# Longitudinal-Predictions-on-ICU-Data
 
- Create_Care_Event.ipynb is used to convert the data from the MIMIC-III database into one-hot encoded care event vectors which can be used to train the LSTM and feed-forward neural networks.

- LSTM_MLP_One-Hot_Vactors.ipynb will take the one-hot encoded care event vectors and train an LSTM model and feed-forward neural network. Before running the code in this notebook, you will need to run the code in Create_Care_Events.ipynb first to get the one-hot encoded care event vectors.

- LSTM_MLP_Autencoder.ipynb contains a stacked autoencoder that will create an embedding from the one-hot encoded care event vectors. T-SNE is used to visualize the autoencoder layers. This file also trains the LSTM and feed forward neural network on the embedding vectors from the autoencoder. Before running the code in this notebook, you will need to run the code in Create_Care_Events.ipynb first to get the one-hot encoded care event vectors.

- Compare_Models.ipynb takes the AUC ROC scores from the models after they are run in LSTM_MLP_One-Hot_Vactors.ipynb and LSTM_MLP_Autencoder.ipynb and craetes visualizations to compare the results.

- The Model_Scores folder contains the AUC ROC scores from running the code in LSTM_MLP_Autencoder.ipynb and LSTM_MLP_One-Hot_Vactors.ipynb. You can use these scores to run the code in Compare_Models.ipynb.
