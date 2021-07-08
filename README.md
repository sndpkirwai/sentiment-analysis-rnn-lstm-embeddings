# sentiment-analysis-rnn-lstm-embeddings

Dataset: Dataset of movie reviews, accompanied by sentiment labels: positive or negative.

Steps:

 --> Load and visualize the dataset
 
 --> 	Data pre-processing:  Get rid of periods, capitalization & punctuations so that we can combined all the reviews back together into one big string
 
 --> 	Encoding the words: Create dictionaries that map the words in the vocabulary to integers. Then, convert each of reviews into integers so they can be passed into the network.
 
 --> 	Removing Outliers: Get rid of extremely long or short reviews; the outliers
 
 --> 	Padding/truncating the remaining data so that we have reviews of the same length
 
 --> 	Preparing Train, Validation & Test dataset
 
 --> 	Prepare Network: 
1.	Embedding Layer – Here need to add an embedding layer because there are huge numbers of words in our vocabulary. It is massively inefficient to one-hot encode that many classes. So, instead of one-hot encoding, we can have an embedding layer and use that layer as a lookup table. You could train an embedding layer using Word2Vec approach, then load it here.

2.	LSTM Layer: Will create an LSTM to use in our recurrent network, which takes in an input_size, a hidden_dim, a number of layers, a dropout probability (for dropout between multiple layers), and a batch_first parameter. For better performance, we will add 2-3 LSTM layer to learn complex relationship.
3.	Fully connected Layer: It takes input as LSTM output and give desired output with the help of sigmoid activation duction.
4.	Binary Cross Entropy Loss: Here we have tried to use new loss, which is designed to work with a single Sigmoid output. BCELoss, or Binary Cross Entropy Loss, applies cross entropy loss to a single value between 0 and 1.
5.	Define hyperparameter: Hit & try n continues...
