# ML3-News-Article-Summarizer
# IITI SoC'21

## Structure of the project-

The Entire code in divided into 5 tasks.

1) Task-1 and Task-2 : Translation of the input news article
2) Task-3 : Summarization of the translated article
3) Task-4 : Generating a heading to the summarized article
4) Task-5 : 

   i)Part A- A code, consisting of all the generated model files, which inputs a news article from the user and gives the user the summarized news article along with a heading.    
   
   ii)Part B- The code also contains a pre-trained model that is used to answer the questions asked by the user, related to the article.

## TASK-1 : tr_en.ipynb- 
#### Purpose and function of tr_en.ipynb- 
Its purpose is to train the model to translate Turkish sentences into English using the wmt16 dataset and "Helsinki-NLP/opus-mt-tr-en" (huggingface) model. We trained this model on a set of Turkish-English sentences so that it will be able to translate Turkish sentences into English with the help of this training. We use this model to translate the input Turkish articles into English.

## TASK-2 : ru_en.ipynb- 
#### Purpose and function of ru_en.ipynb- 
Its purpose is to train the model to translate Russian sentences into English using the wmt16 dataset and "Helsinki-NLP/opus-mt-ru-en" (huggingface) model. We trained this model on a set of Russian-English sentences so that it will be able to translate Russian sentences into English with the help of this training. We use this model to translate the input Russian articles into English.

### Generating Model Files for the Translation part-
To generate the model files that are to be used during translation, we must run and train the two training model codes, i.e, ru_en.ipynb and tr_en.ipynb.

## TASK-3 : summary.ipynb
#### Purpose and function of summary.ipynb-
This colab file is used to train the model to summarize a given English article. It is trained using the "cnn_dailymail" dataset and "facebook/bart-base" model. We will use this model to summarize the output obtained after the translation part.

### Generating Model Files for the Summarization part-
To generate the model files that are to be used during summarization, we must run and train the training model code - summary.ipynb.

## TASK-4 : heading.ipynb
#### Purpose and function of heading.ipynb-
This colab file is used to train the model to set up a heading for a given English article. It is trained using "articles1.csv" dataset from the kaggle site and "t5-base" model. This model is used to create a heading for the output article from the translation part.

### Generating Model Files for the Heading Generation part-
To generate the model files that are to be used for generating the heading, we must run and train the training model code - heading.ipynb.

### Similarity score-
On comparing the output of the trained heading generation model with 20 examples of the "articles1.csv", the similarity score stands out to be 66.66%.

## TASK-5 : final_output.ipynb

This is where the entire project comes together. Talking about the code,

#### Part A:- Translation, Summarization and Heading Generation code

First, it checks the language of the input article and translate it into English, if it is either Russian or Turkish using the generated model files. If it any other language other than English, Russian or Turkish, the program returns "Unsupportable". It break the input article into sentences or parts with less than 512 characters. These are individually passed into the translator and later, combined together using fullstops, to form a paragraph which is in English.

Then, the translated paragraph is summarized. The translated paragraph is broken down into a sets of 5 sentences and sent into the summarizer. The summarized part is finally joined together to get the summarized output.

Next, the translated paragraph is passed through the headline generator to generate a suitable heading for the article.

#### Part B:- Question answering code

A pre-trained question-answering model is used to provide answers to the questions asked by the users. For better efficiency of the answers, the "bert-large-uncased-whole-word-masking-finetuned-squad" model is being used. It asks the users if he/she has any questions related to the article and takes in the questions. With the help of the pre-trained model, it generates the answers.

## Team Members-
1) Snehith Chinta
2) Sharvani Kothuru
3) Shivani Rajaputhra
4) Siddartha Chennareddy

## Mentors-
1) Aryan Rastogi
2) Vardhan Paliwal
