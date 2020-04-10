### Binance API
The Binance is a website that is hosted for cryptocurrency exchange that has
provided a platform for more than 100 cryptocurrencies. at first the binance
company built high frequency trading system for brokers. around 2013 they joined
the blockchain.info as a cryptocurrency wallet's team. now it considered as one
of the biggest cryptocurrency exchange in the world in terms of tradinf volume
We are using their API to get access of the Bitcoin exchange data that is going
on and also the price market of the Bitcoin which is going to be used to train
the Neural Network Model that is predicting the closing price of the Bitcoin the
next day. The method my which Binance API works is that we need to create a
profile for us and login with the credentials given and we need to generate a
APIKey and a SecretKey which are needed to be sent with other needed data
to get the Bitcoin price data. We are using a special module in python for
connecting with API known as binance.client which will be used to send the APIKey
and the SecretKey and get the data back.
