# Sarcasm-in-News-Headlines

In this code, a model is developed to detect sarcasm in news headlines. This model is comprised of four convolutional layers, followed by two GRU and three dense layers. The dataset used for train and validation of the model contains 26709 news headlines, which are categorized into sarcastic and non-sarcastic. The dataset is provided by Kaggle and is available at https://www.kaggle.com/rmisra/news-headlines-dataset-for-sarcasm-detection. To improve the ability of the model to detect the semantic in the news headlines, the 100 dimension version of Global Vectors for Word Representation (GloVe), which is provided by Stanford Natural Language Processing Group, is utilized for embedding the tokenized sentences. The model shows the training accuracy above 98%, and above 85% validation accuracy within 10 epochs.

## Downloaing the News Headlines Dataset For Sarcasm Detection

The News Headlines Dataset For Sarcasm Detection which is used in this project is available at Kaggle. This dataset contains 26709 news headlines, along with the labels for the headlines (1 if the record is sarcastic otherwise 0) and the urls to the articles. To download the dataset, the direct link to the .json file, which is provided by Laurence Moroney (lmoroney@gmail.com / laurencemoroney.com) is utilized. For the purpose of this project, the sentences and their labels are stored in two lists. 

## 
