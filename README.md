# fake-news-detection
This is a machine learning project that aims to classify news as real or fake. The ultimate goal is to feed our passive aggressive classifier directly with data continuously updated from a social media platform (Twitter, for example). However, we will first begin by building a model using data from an available dataset. 

Steps taken to build the model: 
1. Downloading the dataset in a pandas dataframe. 
2. Performing exploratory data analysis on the dataframe to extract insights. 
3. Splitting our data into train and test sets
4. Passing out train set to TfidfVectorizer. This vectorizer converts a collection of raw documents to a matrix of TF-IDF features. These features are defined as follows: 
    a. TF: term frequency, which is the frequency of the occurrence of a term in a document. 
    b. IDF: inverse document frequency, which measures the significance of the term over the entire corpus in such a way that terms such as 'and', 'what', etc. are given lower         significance.
    In formal mathematical terms, TF and IDF can be defined as follows, such that t is a term in a document d from a document set D: 
    ![image](https://user-images.githubusercontent.com/71970059/131371205-8b377fad-1497-40f2-9ee2-b6dd51aed443.png)
5. We pass our TF-IDF matrix to our PassiveAggressiveClassifier. This is a classifier that is usually used with large sets of data as it takes in the data entry by entry, as opposed to taking it in through batches. This classifier is passive when it gets a prediction right, and turns aggressive when a prediction is wrong by attempting to change up the parameters to improve its accuracy. 
6. Assess the performance of our model through multiple metrics. 


