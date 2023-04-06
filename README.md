# Generative Pre-trained Transformer

There are two main limitations to the traditional NLP model:
1. Require a large amount of annotated data, while image labels are not always unique.
2. Models trained for a specific task are difficult to generalize to other tasks.

Therefore, GPT employs a combination of unsupervised and supervised learning as a pre-training objective. <br>
This is commonly known as a generative pre-training model.

## GPT-1
The GPT model was based on Transformer architecture. Unlike other language models,
such as BERT,<br>  which uses the encoder of the Transformer, GPT was made of decoders (12 decoders) stacked on top of each other.

* BERT: encoder of the Transformer; bidirectional model
* GPT: decoder of the Transformer; autoregressive model

### Unsupervised Pre-training:
