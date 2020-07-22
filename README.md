# Sentiment-analysis-of-Reddit-posts
Sentiment analysis of Reddit posts by Natural Language Processing

Social media is one of the most common way for people to express "stress" nowadays. 
This project was trying to conduct a sentiment analysis about stress level of posts from different people.
This porjetc simply posts as binary classification as stressful and non-stressful posts.

Data sources is download from here [A Reddit Dataset for Stress Analysis in Social Media](https://arxiv.org/abs/1911.00133/)

# Run Embedding, F-IDF models, and BERT models
- You can find the training and test data under /data/ folder.
- Pre-processing files are used for word embedding and data clearing.
- Three classifitication mdels can be found under this folder in notebooks. More details about model training are introduced in notebooks.  

# Model training 
 Three feature extraction models TF-IDF, Word2Vec with TF-IDF as weights and BERT were trained in this project. 
 After feature selection, three models including logistic regression, SVM and random forest were applied to classify the binary stress level. 
 
 
# Model results
BERT is the most stable model in this case, with a balanced FP and FN.
Both model can predict whether the text is stressful or non stressful and provide a confidence score.


|Feature Extraction Model	|Best Classification Model	   |  Precision	   | Recall	  |  F1-Score |
| ----------------------- | ---------------------------- | ------------- | ---------| ----------| 
|TF-IDF	                  |Logistic Regression	          | 71.1%	       | 74.4%	     | 74.4%|
|Word2Vec + TF-IDF	       | Random Forest	              |   67.4%	       | 85.8%	    |  76.3%|
|BERT	                 |   Fine Tuning NN	        |       82.7%	     |   81.9%	 |     83.9%|


 For more information, please check notebook.
