# Text summarization 

## Evaluation and Dataset
First we need a metric to evaluate our results. For textsummarisation the rouge score (https://www.aclweb.org/anthology/W04-1013.pdf) is commenly used. This metric counts the matched N-grams. 

Then we need a large dataset which is popular so that we can compare our results. This is fast found and it’s the “cnn daily mail” dataset (https://github.com/abisee/cnn-dailymail).

## Model
After that we need a state of the art language model. The idea is to use a Transformer like Bert to get good results for text summarisation. Now we have a lot to choose from: There is Bert, GPT2, XLNET and many more. There are also higher scaled version like the t5 or even smaller models with state of the art performance like ALBERT or Robert.

### [t5](t5)
I chose the t5 transformer because it was easy to use and I could use the google colab TPU to finetune a pretrained model which has 3B parameters. I got a better rouge score than a Paper from (https://arxiv.org/pdf/1902.09243.pdf) which is from 2019.

### [ALBERT](albert)
Now I wanted try out Albert to see if I could results like the t5 with a much smaller Model, which has similar performance like Bert-Large with 18x fewer parameters and can be trained about 1.7x faster. (https://arxiv.org/abs/1909.11942). But the Albert model is not so easy to use for text summary. 


