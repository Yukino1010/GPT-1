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

<img width="600px" src="https://github.com/Yukino1010/Generative-Pre-trained-Transformer/blob/master/image_source/img1.png" >

In the Unsupervised Pre-training phase, U = {u1, u2, …., uN} represents an unlabeled sequence; <br> 
The model's objective is to predict the next letter based on the preceding context.

### Supervised Fine-Tuning:
<img width="800" src="https://github.com/Yukino1010/Generative-Pre-trained-Transformer/blob/master/image_source/img4.png" >

<img width="600px" src="https://github.com/Yukino1010/Generative-Pre-trained-Transformer/blob/master/image_source/img2.png" >

In this phase, C represents a labelled dataset that can be used to fine-tune the pre-trained model <br>
for specific NLP tasks such as semantic similarity, textual entailment, and document classification.

<img width="600px" src="https://github.com/Yukino1010/Generative-Pre-trained-Transformer/blob/master/image_source/img3.png" >

The authors did not directly use L2 but instead incorporated L1 and used λ (0.5) to adjust the weights between the two tasks.

## GPT-2, GPT-3
GPT-2 and GPT-3 are the second and third generations of the Generative Pre-Training (GPT) model. <br>
The architecture of these models is similar to GPT-1 but includes more decoder layers and was trained on a larger dataset, <br>
resulting in an increase in the number of parameters.

### GPT-2
1. Parameter: 1.5B, Data Size: 40 GB
2. Training objective transfer from P(output|input) to P(output|input, task)
3. Zero-Shot Learning

### GPT-3
1. Parameter: 175B, Data Size: 45 TB
2. In-context learning
3. Few-shot, one-shot and zero-shot learning

## Reference
