# Anomaly Detection Using Autoencoders With Metro do Porto Dataset
Implementation of various types of Autoencoders to the Porto Metro dataset (found at https://archive.ics.uci.edu/dataset/791/metropt+3+dataset). The data preparation for different months was done in different files, each with a self-explanatory name.

First the dataset was fed into a sparse autoencoder, the code for which can be found at Porto_SAE.ipynb.

However, since this is sequential data (i.e. following a time series), we thought it appropriate to construct an autoencoder with LSTM architecture, which is generally better at handling time-sequential data, the code for which can be found at Porto_LSTM.ipynb.

In both cases, a custom-built function loss was used, which included the Frobenius loss, as well as the Kullback-Leibler divergence, as well as the usual mean squared error. This loss was first studied for the case of a simple electrocardiogram dataset, and the code can be found at loss_function_study(ECG).ipynb
