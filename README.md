# Forecasting Nord Pool's Day-ahead hourly spot prices in Finland

This repository contains notebooks and scripts related to the thesis.

The encoder-decoder LSTM can be trained with Pandas Dataframes that are saved to a pickle file. In the dataframe, the target variable needs to be on the first column, followed by other features in their own columns.

```shell
python LSTM_Encoder_Decoder.py --dataset dataset.pickle --hparams hyperparameters.txt --cnn
```

The dataset needs to be a Pandas Dataframe that is saved as a pickle (pandas.to_pickle). The first column of the dataset needs to be the target, spot price, other columns act as features.

An example of the hyperparameters.txt file is in the scripts folder. The --cnn parameter uses the CNN-LSTM model architecture, leaving the parameter out uses the LSTM encoder-decoder architecture.