### Importing the modules
The first and foremost thing to do is to import all the necessary modules
into the program so we can use to program the neural Network

``` python
import pandas as pd
from sklearn.preprocessing import MinMaxScaler
import numpy as np
import matplotlib.pyplot as plt
import tensorflow as tf
from keras.models import Sequential
from keras.layers import LSTM,Dense
from binance.client import Client
```

### Getting the Data From the API
We are using a Proprietary module to get the Data fromt he binance and
also store the data the data in the local system

``` python
client = Client(APIKey,SecretKey)
symbol = "BTCUSDT"
BTC = client.get_historical_klines(symbol=symbol,interval=Client.KLINE_INTERVAL_30MINUTE,start_str="1 year ago UTC")
```

### Normalize the Data
The sklearn is used to normalize the data and also use it to change the normalized data
to the main state

``` python
scaler = MinMaxScaler()
data = scaler.fit_transform(data)
```

### Creating the model
To create the model we are using the keras modules to get the necessary function and also the
compatible data type we are using three layers which are input node contains 256 neuron
and the hidden layer has 256 neurons and at the last we have the one output neuron

``` python
model = Sequential()
model.add(LSTM(256,return_sequences=True,input_shape=(x_train.shape[1],x_train.shape[2])))
model.add(LSTM(256))
model.add(Dense(1))
```

### Visualize the data
The Visualization is used to represent the data that is predicted in a more
GUI format that will make the prediction more and more user friendly to use

``` python
plt.figure(figsize=(20,8))
plt.plot(predicted_price,color="red",label="predicted price")
plt.plot(real_price,color="blue",label="Real Price")
plt.title("prediction vs Real")
plt.xlabel("time")
plt.ylabel("price")
plt.show()
```
