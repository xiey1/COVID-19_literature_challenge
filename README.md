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
   WordNetLemmatizer
   ScispaCy
   https://allenai.github.io/scispacy/
   https://spacy.io/usage/spacy-101

### Embedding models:
   Latent Dirichlet Allocation (LDA)
   Latent Semantic Analysis (LSA)
   BioBERT
<br>**Note:** For LDA and LSA, a variety of different topic numbers (10,20,30,40,50,100) have been tested.

