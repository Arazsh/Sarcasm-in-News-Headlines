# Sarcasm-in-News-Headlines

In this code, a model is developed to detect sarcasm in news headlines. This model is comprised of four convolutional layers, followed by two GRU and three dense layers. The dataset used for train and validation of the model contains 26709 news headlines, which are categorized into sarcastic and non-sarcastic. The dataset is provided by Kaggle and is available at https://www.kaggle.com/rmisra/news-headlines-dataset-for-sarcasm-detection. To improve the ability of the model to detect the semantic in the news headlines, the 100 dimension version of Global Vectors for Word Representation (GloVe), which is provided by Stanford Natural Language Processing Group, is utilized for embedding the tokenized sentences. The model shows the training accuracy above 99%, and above 85% validation accuracy within 10 epochs.

## Downloaing the News Headlines Dataset For Sarcasm Detection

The News Headlines Dataset For Sarcasm Detection which is used in this project is available at Kaggle. This dataset contains 26709 news headlines, along with the labels for the headlines (1 if the record is sarcastic otherwise 0) and the urls to the articles. To download the dataset, the direct link to the .json file, which is provided by Laurence Moroney (lmoroney@gmail.com / laurencemoroney.com) is utilized. For the purpose of this project, the sentences and their labels are stored in two lists. 

## Tokenizer

The next step is tokenizing the words in the sentences. The analysis shows that there exist 29656 unique words in the dataset. Then, the sentences (headlines) are converted to sequences using the tokenized words. The longest sentence in the dataset is comprised of 40 words. In oder to make the length of all sequences the same, the shorter sentences are zero-padded by 'post' format. Next, the data is sliced for training and validation. I allocated 80% of the data for training, and the rest for validation.

## Downloading the GloVe

Global Vectors for Word Representation (GloVe) is an unsupervised learning algorithm for obtaining vector representations for words. Training is performed on aggregated global word-word co-occurrence statistics from a corpus, and the resulting representations display interesting linear substructures of the word vector space [[Ref](https://nlp.stanford.edu/pubs/glove.pdf)].To improve the ability of the model to detect the semantic in the news headlines, the 100 dimension version of GloVe 6B (vocab size = 400k), which is provided by Stanford Natural Language Processing Group, is utilized for embedding the tokenized sentences. The direct linke is provided by Laurence Moroney.

##  Building the model

The model initiates the process with an embedding layer of weights that produced by the 100d GloVe. Then, four 1D convolutional blocks are installed. Each convolutional block consists of one Conv1D which is followed by a BatchNormalization layer and a rectified linear activation function ReLU. Then, two GRU layers are used that each of them is followed by a Dropout layer. Finally, four Dense layers and two dopout layers that reduce the overfitting are used.  
Next, to make the training and validation sequences usable by the model, they are converted to numpy arrays. For fitting the model, the Adam and binary crossentropy are respectively used for optimizer and loss function. The model shows the training accuracy above 99%, and above 85% validation accuracy within 10 epochs.

## Plot accuracy/loss vs. epochs

Finally, the variations of accuracy and loss versus epochs for both training and validation sets are plotted. The plots are as follows:

