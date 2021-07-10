# ML3-News-Article-Summarizer
# IITI SoC'21
## 1)Training Models-
### i)ru_en.ipynb-
Purpose and function of ru_en.ipynb is to train the model to translate Russian sentences into English using the wmt16 and hugging face datasets. We train this model on some set of Russian-English sentences so that it will be able to translate Russian sentences into English with the help of this training. So, we call this model to translate Russian to English.
### ii)tr_en.ipynb-
Purpose and function of tr_en.ipynb is to train the model to translate Turkish sentences into English using the wmt16 and hugging face datasets. We train this model on some set of Turkish-English sentences so that it will be able to translate Turkish sentences into English with the help of this training. So, we call this model when we need to translate Turkish to English.

## 2)Generating Model Files-
To generate the model files that are to be used during translation, we must run and train the two training model codes, i.e, ru_en.ipynb and tr_en.ipynb.

## 3)Translation Code-
### translation.ipynb - 
The purpose of this file is to produce translated output of the input as a string and store it. It first identifies the language and then breaks down paragraphs into sentences. If the sentence has more than 512 characters, it would break it into parts with less than 512 characters. After splitting into sentences with parts having less than 512 characters, we translate the given language into English using the model files generated and then join all the sentences to form a paragraph. The output is stored as a string in a certain variable to be used for further processing.

## Team Members-
1) Snehith Chinta
2) Sharvani Kothuru
3) Shivani Rajaputhra
4) Siddartha Chennareddy
