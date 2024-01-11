# AlmaBetter-Topic-Modeling-Of-News-Articles 
In this project we are given a collection of BBC news articles which belongs to four different categories (business, sport, tech, entertainment, and politics) in seperate folders. The first step is to aggregate these articles into single dataframe containing category, content, and title. Secondly, we check for missing values, unique terms, and visualize the word count of title and article length in each category to understand the data better. Then we combine all the text data into single column which is used in feature engineering and model building. In feature engineering we do text pre-processing where expand contractions, remove digits, remove white spaces, remove URLs, remove stop words, converting into lower case. Now the text is ready to undergo few changes that a computer can understand the data. It involves tokenization, normalization and vectorization after which we obtain the final document term matrix of the text column. Now this matrix is used in model building using LDA with count vectorizer, LDA with TF-IDF vectorizer, LSA with count vectorizer, and LSA with TF-IDF vectorizer. On observing word cloud and top words in each topic we can understand in which category the topic falls under. Finally, given categories and the topics obtained are verified.
# Table of contents
* Data cleaning and manipulation
* Data Visualizations
* Feature Engineering 
* Model implementation
* Conclusion 
* Tools
# Data cleaning and manipulation
* Initally, there are seperate files for business, entertainment, politics, sport, and tech in which news are stored. Then we combined these files and created a single dataframe by performing few manipulations from which the dataset has 2225 rows and 3 columns (Headline, Description, and Category).
* Then we found 100 duplicates in the dataset, so we removed them. Therefore, now the dataset has 2125 rows and 3 columns.
* All the text is stored in a single column named Description so that while performing topic modeling it will be easy to analyze the topics.
# Data Visualizations
* Distribution of articles over categories
* Word cloud of a headline column
* Article length of categories
# Feature Engineering
# Text Pre-processing 
* In expand contractions section, we have imported contractions library to expand the words.
* Then we converted the entire text to lower case so that consistency is maintained.
* Then we removed punctuations, digits, and whitespaces.
* To obtain proper accuracy we have removed most frequently used words which are called as stop words.
* Tokenization is performed to the text and visualized the top 10 most frequently used words.
* Now we normalised the text column using lemmatizer so that similar words are replaced by a one common meaningful word.
* Then vecrorization is perfomed for the text using both count vectorizer and TF-IDF (Term frequency - inverse document frequency) vectorizer.
# Model Implementation
Now coming to the model implementation, following are the models used.
* LDA with count vectorizer
* LDA with TF-IDF vectorizer
* LSA with count vectorizer
* LSA with TF-IDF vectorizer
# Conclusion
## Conclusion from EDA
First we performed feature engineering which involves majorly a text pre-processing since the dataset is completely of text.
* The steps involved in text processing are expand contractions, remove urls, remove digits, convert text to lower case, remove stopwords, tokenization, text normalization using lemmatizer, and text vectorization using count vectorizer and TF-IDF vectorizer.
* Finally coming to the model implementation and their respective evaluation metrics. Here we considered perplexity score as evaluation metrics for LDA and distribution of topics to documents for LSA. 
1. LDA with count vectorizer
* perplexity score - 748.620 
2. LDA with TF-IDF vectorizer
* perplexity score - 2180.565 
3. LSA with count vectorizer 
* 0   - 2001
* 1   -  15
* 2   -  65
* 3   -  30
* 4   -  14
4. LSA with TF-IDF vectorizer 
* 0  -  1914
* 1  -   19
* 2  -   83
* 3  -   67
* 4  -   42 
Therefore, On comparing the models built, we noticed that LDA with count vectorizer performed better with low perplexity score. Also, looking at the topic distribution LDA has assigned topics accurately with high accuracy.
# Tool
Google colab 
