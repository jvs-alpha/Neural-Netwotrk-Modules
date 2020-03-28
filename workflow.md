### Workflow
The first step is to get the data from the source
to get the data from the website we are using urllib and a proprietary
API module known as the  binance.client which will use a private and public
key to access and get the data from their database. the next step is to store the
in the localsystem with a standard method for data collection so we are using
CSV format for storing the data from the server. The third step is to normalize
the data which we are going to used to train the neural network with we are using
sklearn module to normalize the data. we are also using the numpy module for
intermediate communication from the sklearn and the tensorflow library
. the fourth we are using the tensorflow library's sub modules keras to make and
train the module. fifth step is to reverse the process of the normalization
and transform the data to the original state. Finally we are testing the data
with the trained model and displaying the output using the matplotlib for
graphical view
