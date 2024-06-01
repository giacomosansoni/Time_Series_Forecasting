# Time-Series

In this homework we were asked to predict future samples of the input time series implementing forecasting models to learn how to exploit past observations in the input sequences to correctly predict the future. We were provided of only the train set, to be used to learn the models. The submissions were then evaluated on a hidden test set.

## Files in the Repository

-  **Dataset.ipynb**: Focused on data preparation and preprocessing. It creates subsequences from the original time series based on valid periods specified. These subsequences are labeled with their corresponding categories. rows with a high proportion of zeros are filtered. The dataset is reorganized so that categories are mixed uniformly.
-  **Conv1DResnet_BahdanuAttention.ipynb**: A model using 1D convolutional layers (Conv1D) and custom Bahdanau attention layer. The architecture utilizes the ResNet-like approach with skip connections and batch normalization.
-  **LSTM_Conv1D_&_Dense_Models.ipynb**: A first model combines bidirectional LSTMs and dense layers to predict time series data. A second one introduces convolutional layers alongside the LSTM layers. A third one incorporates a custom attention layer that computes context vectors from the LSTM outputs.
-  **Autocorrelation_Layer.ipynb**: A PreviousInputLayer manages autocorrelation by integrating a trainable parameter (rho) and a non-trainable state (previous_input) to modify the input based on the last input batch, intended to capture temporal dependencies within the data. T2V (Time2Vector) transforms time series data into a representation that includes both linear and periodic components, enhancing the model's ability to handle periodic patterns in the data.
