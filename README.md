# ML3-News-Article-Summarizer
Purpose and function of ru_en.ipynb is to train the model to translate russian sentences into english sentences using the wmt16 and hugging face datasets.So we call this model to translate russian to english.
Purpose and function of tr_en.ipynb is to train the model to translate turkish sentences into english sentences using the wmt16 and hugging face datasets.So we call this model to translate turkish to english.
translation.ipynb, the purpose of this file is to produce translated output of input as a string. It first identifies the language and then breakdown paragraphs into sentences. If the sentence has more than 512 characters, it would break it into other more parts. After splitting, we translate the given language into english language and then join all the sentences with full stops. And the output is stored as a string.
To generate model files, one must run the two traning model codes to generate it.
