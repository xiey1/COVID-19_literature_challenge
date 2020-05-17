# COVID-19_literature_challenge
Text embedding for COVID-19 literature
<br>Data source: https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge

<br>This project has 5 sections with code and detailed explanation in 5 jupyter notebooks.

* **Part I: Data cleaning and exploratory data analysis**
<br>Load and compile text data from json files. Perform data cleaning, filtering and exploratory data analysis.
* **Part II: Latent Dirichlet Allocation (LDA)**
<br>Perform Latent Dirichlet Allocation (LDA) analysis on abstracts and bodytext with a variety of different topic numbers. Embed abstracts and bodytext in the topic space and validate embedding performance using titles/abstracts/bodytext from the same paper.
* **Part III: Latent Semantic Analysis (LSA) -- Gensim**
<br>Perform Latent Semantic Analysis (LSA) on abstracts and bodytext with a variety of different topic numbers using Gensim package. Embed abstracts and bodytext in the LSA space and validate embedding performance using titles/abstracts/bodytext from the same paper.
* **Part IV: Latent Semantic Analysis (LSA) -- sklearn**
<br>Perform Latent Semantic Analysis (LSA) on abstracts and bodytext with a variety of different topic numbers using sklearn package.
* **Part V: BioBERT**
<br>Embed abstracts and bodytext using pre-trained weights from BioBERT.

# Project Aim:
### Create an algorithm to embed biomedical articles and help with literature search based on semantic meanings
The massive amount of articles on COVID-19 is overwhelming for researchers and other readers to find useful information. To facilitate the literature search process, different text embedding methods have been performed to help identify the most relevant article.

# Approach:
### Text processing methods:
1. WordNetLemmatizer
2. ScispaCy
<br>https://allenai.github.io/scispacy/
<br>https://spacy.io/usage/spacy-101

### Embedding models:
1. Latent Dirichlet Allocation (LDA)
2. Latent Semantic Analysis (LSA)
3. BioBERT
<br>**Note:** For LDA and LSA, a variety of different topic numbers (10,20,30,40,50,100) have been tested.

## Part I: Data cleaning and exploratory data analysis
### Cleaning steps and number of literature in each step:
<br>Number of literature in 'metadata.csv': 47298
<br>Number of literature in json files: 52097
<br>Number of literature shared in 'metadata.csv' and json files: 32417
<br>Number of literature containing title, abstract and bodytext with Pubmed ID: 21600
<br>Number of literature in English: 21423

### Exploratory data analysis:
* Distribution of the number of literature published in each year
<img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/Publication_by_year.png' width=600px>

* Distribution of wordcount in titles, abstracts and bodytext
<img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/wordcount_distribution.png' width=600px>

## Part II: Latent Dirichlet Allocation (LDA)
Two text preprocessing methods have been employed **WordNetLemmatizer** and **ScispaCy**. Both mothods yield comparable wordcount in titles, abstacts and bodytext after preprocessing.
<img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/wordcount_distribution_preprocessing.png' width=600px>

<br>Number of literature in each topic
<img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/LDA_topic_distribution.png' width=800px>

<br>Cumulative distribution of topic classification accuracy
<img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/LDA_topic_classification_accuracy_cumulative.png' width=800px>

<br>With cosine similarity score as evaluation metric, compare the cosine similarity rank between title, abstract and bodytext for each paper using different LDA methods.

<br>**WordNetLemmatizer** vs **ScispaCy**
<img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/LDA_cosine_similarity_rank_method.png' width=800px>

<br>Topic number
<br><img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/LDA_cosine_similarity_rank_topic_number.png' width=800px>

## Part III: Latent Semantic Analysis (LSA) -- Gensim
<br>With cosine similarity score as evaluation metric, compare the cosine similarity rank between title, abstract and bodytext for each paper using different LSA methods from Gensim.

<br>**WordNetLemmatizer** vs **ScispaCy**
<img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/LSA_cosine_similarity_rank_method.png' width=800px>

<br>Topic number
<br><img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/LSA_cosine_similarity_rank_topic_number.png' width=800px>

## Part IV: Latent Semantic Analysis (LSA) -- sklearn
<br>With cosine similarity score as evaluation metric, compare the cosine similarity rank between title, abstract and bodytext for each paper using different LSA methods from sklearn.

<br>**WordNetLemmatizer** vs **ScispaCy**
<img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/LSA_sklearn_cosine_similarity_rank_method.png' width=800px>

<br>Topic number
<br><img src= 'https://github.com/xiey1/COVID-19_literature_challenge/blob/master/images/LSA_sklearn_cosine_similarity_rank_topic_number.png' width=800px>





