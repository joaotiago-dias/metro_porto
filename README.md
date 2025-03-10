# Anomaly Detection Using Autoencoders With Metro do Porto Dataset
Implementation of various types of Autoencoders to the Porto Metro dataset (found at https://archive.ics.uci.edu/dataset/791/metropt+3+dataset). The data preparation for different months was done in different files, each with a self-explanatory name.

To begin with, the data preparation was done (at data_preparation.ipynb) and the resulting outputs were saved to the 'npy_files' folder. A +reliminary study of autoencoders was also undertaken, for which the relevant notebook is loss_function_study(ECG).ipynb

Two types of autoencoder architecture were implemented: Sparse autoencoders (SAE) and long short term memory (LSTM) autoencoders, which better take into account the sequential nature of the data.

For the SAE impementation, we have examples of a straightforward implementation (Porto_SAE.ipynb), an implementation with moving windows (Porto_SAE_window.ipynb), an implementation which employed a low pass filter to the results of the encoder (Porto_SAE_LPF.ipynb), and a version which combines the moving window with the low pass filter (Porto_SAE_window_v2.ipynb).

For the LSTM implementation, we have a straightforward implementation (Porto_LSTM.ipynb), as well as a moving windows application of LSTM (Porto_LSTM_window.ipynb -- although this implementation updates the autoencoder more than once per hour, which, over many months, makes for a really long computation time (3-4 days)).
