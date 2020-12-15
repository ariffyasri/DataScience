# sentiment-analysis-using-malaya

To show how to utilize Malaya repo for sentiment analysis

# Introduction

[Malaya](https://github.com/huseinzol05/Malaya) is a Natural-Language-Toolkit library for bahasa Malaysia, powered by Deep Learning Tensorflow.

[Sentiment Analysis](https://en.wikipedia.org/wiki/Sentiment_analysis) (also known as opinion mining or emotion AI) refers to the use of natural language processing, text analysis, computational linguistics, and biometrics to systematically identify, extract, quantify, and study affective states and subjective information.

# Why this ReadMe exist?

Malaya library is very good, but not so friendly (some module less documentation) for me as a beginner to play around with the example given. So I make this repo as a record for future. :)

# Sentiment analysis Using Malaya

In this example, I will use Bidirect Encoder Representation from Transformer (BERT).

There are several scenario in the example:

1. How to create our own pretrain model?
2. How to finetune pretrain model?

This example is from this [commit](https://github.com/huseinzol05/Malaya/tree/dc2160711625740573b5feb48d9d970dc704e763). This is to make sure that all the steps below can be recreated without any issues such as deleted file, renamed file, moved file to other folder, etc.

# How to create our own pretrain model?

1. Go to here https://github.com/huseinzol05/Malaya/tree/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/bert#how-to
2. Follow the steps

Notes:

* Please change directory accordingly, such as the text file to be read, config file, etc.
* If you want to download the pretrain model, can refer to here: https://github.com/huseinzol05/Malaya/tree/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/bert#download


# How to finetune pretrain model?

1. There are two example 
    
    * https://github.com/huseinzol05/Malaya/blob/dc2160711625740573b5feb48d9d970dc704e763/finetune/bert/tf-estimator-text-classification.ipynb which using WordPiece tokenizer or 
    
    * https://github.com/huseinzol05/Malaya/blob/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/bert/how-to-classification.ipynb which using SentencePiece tokenizer
2. Follow the steps
    
    * If you want to create your own WordPiece tokenizer, you can go to here https://github.com/huseinzol05/Malaya/blob/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/bert/build-wordpiece.ipynb

    * If you want to create your own SentencePiece tokenizer which will create vocab and model, can go to here https://github.com/huseinzol05/Malaya/tree/dc2160711625740573b5feb48d9d970dc704e763/pretrained-model/preprocess#generate-preprocessing-texts

    * If you have more labels in dataset, and to finetune it with added labels, then you may change the variable `logits` value in `model_fn` function to number of labels you have. https://github.com/huseinzol05/Malaya/blob/dc2160711625740573b5feb48d9d970dc704e763/finetune/bert/tf-estimator-text-classification.ipynb

        example: ```logits = tf.layers.dense(output_layer, 3) # 3 labels```

Notes:

* Most the steps will use helper scripts which has been wrote by the author to ease other developers to play around with the library

If have time, I will prepare the example :)