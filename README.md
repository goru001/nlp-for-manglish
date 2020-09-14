# NLP for Manglish (Code mixed Malayalam+English)

This repository contains state of the art Language models and
 Classifier for Code mixed Manglish (Malayalam and English) - 
 spoken in Indian sub-continent. 
  
  
## Dataset

1. [Malayalam Wikipedia Articles](https://www.kaggle.com/disisbig/malayalam-wikipedia-articles) : 
Preprocessed, Transliterated and Translated versions of this dataset, used for 
language modeling in this repo, can be downloaded directly from [here](https://drive.google.com/drive/folders/1M4Sx_clF0iP1y-JG3OhfacFKTDoHXCR1?usp=sharing)

2. [Dravidian Codemix HASOC @ FIRE 2020](https://sites.google.com/view/dravidian-codemix-fire2020/overview)

3. [Dravidian Codemix Sentiment Analysis @ FIRE 2020](https://dravidian-codemix.github.io/2020/)


## Results

### Language Model Perplexity (on validation set)


| Architecture/Dataset | Malayalam Wikipedia Articles | Malayalam Wikipedia Articles |
|:--------------------:|:----------------------------:|:----------------------------:|
|                      |         Latin Script         |         Mixed Script         |
|        ULMFiT        |             45.84            |             41.22            |


### Classification Metrics

##### ULMFiT

| Dataset | F1 | Precision | Recall | Notebook to Reproduce results |
|:--------:|:----:|:----:|:----:|:----:|
| Dravidian Codemix HASOC @ FIRE 2020 (Latin Script) |  0.74  |  0.76  |  0.72  | [Link](https://github.com/goru001/nlp-for-manglish/blob/master/classification/classification_model_hasoc.ipynb) |
| Dravidian Codemix HASOC @ FIRE 2020 (Mixed Script) |  0.91  |  0.92  |  0.91  | [Link](https://github.com/goru001/nlp-for-manglish/blob/master/classification/classification_model_hasoc.ipynb) |
| Dravidian Codemix Sentiment Analysis @ FIRE 2020 |  0.69  |  0.69 | 0.7 | [Link](https://github.com/goru001/nlp-for-manglish/blob/master/classification/classification_model_dc_fire.ipynb) |


### Visualizations
 
##### Word Embeddings

| Architecture/Dataset |                                                                                   Malayalam Wikipedia Articles                                                                                  |                                                                                   Malayalam Wikipedia Articles                                                                                  |
|:--------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
|                      |                                                                                           Latin Script                                                                                          |                                                                                           Mixed Script                                                                                          |
|        ULMFiT        | [Embeddings projection](https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/goru001/nlp-for-manglish/master/language-model/embedding_projector_config_latin_script.json) | [Embeddings projection](https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/goru001/nlp-for-manglish/master/language-model/embedding_projector_config_mixed_script.json) |


## Pretrained Models

#### Language Models 

Download Latin script pretrained ULMFiT LM from [here](https://drive.google.com/drive/folders/1heJyR6_lfVa_3KcnRwo45C6moCkPYXxd?usp=sharing)

Download Mixed Script pretrained ULMFiT LM from [here](https://drive.google.com/drive/folders/1v7ZTfjzhO5rz2OC8-qtgSdP3nv_JAdwt?usp=sharing)

#### Tokenizer

Trained tokenizer using Google's [sentencepiece](https://github.com/google/sentencepiece)

Download the trained model and vocabulary for both Latin and Mixed scripts
 from [here](https://drive.google.com/drive/folders/1zZsRR56jU1P-iVsJGyHli9MxMhALzXhi?usp=sharing)
