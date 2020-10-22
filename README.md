# Sarcasm-in-News-Headlines

In this code, a model is developed to detect sarcasm in news headlines. This model is comprised of four convolutional layers, followed by two GRU and three dense layers. The dataset used for train and validation of the model contains 26709 news headlines, which are categorized into sarcastic and non-sarcastic. The dataset is provided by Kaggle and is available at https://www.kaggle.com/rmisra/news-headlines-dataset-for-sarcasm-detection. To improve the ability of the model to detect the semantic in the news headlines, the 100 dimension version of Global Vectors for Word Representation (GloVe), which is provided by Stanford Natural Language Processing Group, is utilized for embedding the tokenized sentences. The model shows the training accuracy above 98%, and above 85% validation accuracy within 10 epochs.

## Downloaing the News Headlines Dataset For Sarcasm Detection

The News Headlines Dataset For Sarcasm Detection which is used in this project is available at Kaggle. This dataset contains 26709 news headlines, along with the labels for the headlines (1 if the record is sarcastic otherwise 0) and the urls to the articles. To download the dataset, the direct link to the .json file, which is provided by Laurence Moroney (lmoroney@gmail.com / laurencemoroney.com) is utilized. For the purpose of this project, the sentences and their labels are stored in two lists. 

## Tokenizer

The next step is tokenizing the words in the sentences. The analysis shows that there exist 29656 unique words in the dataset. Then, the sentences (headlines) are converted to sequences using the tokenized words. The longest sentence in the dataset is comprised of 40 words. In oder to make the length of all sequences the same, the shorter sentences are zero-padded by 'post' format. Next, the data is sliced for training and validation. I allocated 80% of the data for training, and the rest for validation.

## Downloading the GloVe

GloVe is an unsupervised learning algorithm for obtaining vector representations for words. Training is performed on aggregated global word-word co-occurrence statistics from a corpus, and the resulting representations showcase interesting linear substructures of the word vector space [[Ref](https://nlp.stanford.edu/pubs/glove.pdf)].To improve the ability of the model to detect the semantic in the news headlines, the 100 dimension version of Global Vectors for Word Representation (GloVe), which is provided by Stanford Natural Language Processing Group, is utilized for embedding the tokenized sentences.

