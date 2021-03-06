##Overview
The aim of this project was to build a recommender system that will take a user's saved vocabulary list and recommend texts for her to read, based on the vocabulary saved, and based on her explicitly stated interests. It is aimed at all learners of the Chinese language. Texts stored in the inverted index vary in length from one sentence to lengthier documents.   
  
The system will recommend the user a Chinese text sourced online if the majority of that text is comprised of words in his vocabulary list, and if the topic of the text corresponds to his explicitly stated interests. Returning documents that are mostly comprised of the user's known vocabulary is ideal, as the majority of the document can be read by the user without much effort. 
  
The user can choose to read the text as is, or the remaining unknown characters can be translated; this way, reading the document is not as daunting a task, because these unknown characters will be a smaller percentage of the text overall. If the majority of the document is unknown to the user, gaining full comprehension of the document could be taxing and time-consuming for the reader. 
  
The system will first locate texts in the inverted index that are mostly comprised of the user's saved vocabulary. The documents would ideally be sourced on the web and indexed using a Web Scraper. However, for this prototype, the documents were manually sourced from various online corpora, and indexed locally using Solr. When the Solr inverted index is queried, these documents will then be weighted and ranked according to how similar they are to the user's interests.  
  
Initially, finding texts that correspond to the user's vocabulary will rely on a keyword approach (content-based filtering). The approach to ranking the text based on a user's interests, however, will be based on an ontological approach, whereby synonyms of the user's topics of interest will be taken into account when ranking the document. For example, if the user specifies skiing as an interest, a text on the topic of winter sports or containing the words ``winter sports'' will likely be ranked higher in the list. 
  
**Main Python modules used for this project:**  
SnowNLP - Chinese text processing library  
microsofttranslator - API for Microsoft Translator  
NLTK interface to the Princeton Wordnet lexical dictionary  
