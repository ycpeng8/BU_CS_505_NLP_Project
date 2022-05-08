# BU_CS_505_NLP_Project

Team members: Guangyue Qiu, Guankai Sang, Yanchong Peng, Yufan Lin, Zhenghang Yin, Juncheng Zhang

## Project report and presentation slides

Report: [Paper.pdf](Paper.pdf)

Presentation Slide: [main_figure.pptx](main_figure.pptx)

## Task Description

Multilingual Twitter sentiment classification. Data of English tweets annotated with their sentiment can be found in this [link](http://help.sentiment140.com/for-students/): noisy data automatically annotated with sentiment based on emojis, and in this [link](https://www.dropbox.com/s/byzr8yoda6bua1b/2017_English_final.zip?file_subpath=%2F2017_English_final%2FGOLD%2FSubtask_A): clean data annotated by human (Amazon Mechanical Turk) annotators, from SemEval sentiment analysis in Twitter (task A) – you need to download several files from 2013, 2014, 2015, and 2016. Data of Arabic tweets annotated with their sentiment can be found in this [link](https://www.dropbox.com/s/i9tkaajuq1qbgjq/2017_Arabic_train_final.zip?file_subpath=%2F2017_Arabic_train_final%2FGOLD) from SemEval sentiment analysis in Twitter (task A). Project ideas based on these datasets include: 

Comparing the performance on the same test sets (from SemEval 2017), of models trained with noisy data vs. clean data. Then, building models to explore if pre-training models with the noisy data and then fine-tuning them with the clean data can improve performance (see [here](https://arxiv.org/abs/1901.11373) for inspiration why this is an interesting question).

## Files Instructions

1. Bert-tiny model
    - [***bert_tiny_noisy_data.ipynb***](bert_tiny_noisy_data.ipynb) Train the Bert-tiny model on the noisy data
    - [***bert_tiny_clean_data.ipynb***](bert_tiny_clean_data.ipynb) Train the Bert-tiny model on the clean data
    - [***bert_tiny_finetuning_data.ipynb***](bert_tiny_finetuning_data.ipynb) Finetune the Bert-tiny model (pretrained on the noisy data) on the clean data

2. xlnet-tiny model
    - [***xlnet_noisy_data.ipynb***](xlnet_noisy_data.ipynb) Train the xlnet-tiny model on the noisy data
    - [***xlnet_clean_data.ipynb***](xlnet_clean_data.ipynb) Train the xlnet-tiny model on the clean data
    - [***xlnet_finetuning_data.ipynb***](xlnet_finetuning_data.ipynb) Finetune the xlnet-tiny model (pretrained on the noisy data) on the clean data

3. DistilGpt2 model
    - [***distilgpt2_noisy_data.ipynb***](distilgpt2_noisy_data.ipynb) Train the DistilGpt2 model on the noisy data
    - [***distilgpt2_clean_data_and_finetuning_2_classes.ipynb***](distilgpt2_clean_data_and_finetuning_2_classes.ipynb) There are **two** classes (positive, negative) of sentiment in the clean data. Train the DistilGpt2 model on the clean data. Then, finetune the noisy model (pretrained in [*distilgpt2_noisy_data.ipynb*](distilgpt2_noisy_data.ipynb)) on the clean data
    - [***distilgpt2_clean_data_and_finetuning_3_classes.ipynb***](distilgpt2_clean_data_and_finetuning_3_classes.ipynb) There are **three** classes (positive, neutral, negative) of sentiment in the clean data. Train the DistilGpt2 model on the clean data. Then, finetune the noisy model (pretrained in [*distilgpt2_noisy_data.ipynb*](distilgpt2_noisy_data.ipynb)) on the clean data

> ***Note*** The above models are all tested on the clean data