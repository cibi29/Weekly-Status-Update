# Weekly-Status-Update
This page will temporary reflect weekly updates on the project

## Week 1
* Read the Active Learning Survery by Burr Settles
* Read the following papers - 
1. [Efficient Estimation of Word Representations in Vector Space](https://arxiv.org/pdf/1301.3781.pdf)
2. [word2vec Parameter Learning Explained](https://arxiv.org/pdf/1411.2738v3.pdf)
3. [Training Connectionist Networks with Queries and Selective Sampling](https://papers.nips.cc/paper/261-training-connectionist-networks-with-queries-and-selective-sampling.pdf)
* Word2vec was evaluated for different sizes of training dataset from 0.1 to the entire dataset. [Results](https://user-images.githubusercontent.com/27007966/28961123-d26b81c4-791e-11e7-8313-b3e05f6be733.png)
* As expected, performance increases almost linearly with the size of the training dataset. 

## Week 2 (In Progress)
* Goal - Machine Translation from French to English to augment English dataset
* Reading about - 
1. FastText - Results on its performance with respect to word2vec on benchmarks. [Link](https://rare-technologies.com/fasttext-and-gensim-word-embeddings/)
2. Convolutional Sequence to Sequence Learning (Neural Machine Translation at Facebook)
3. Google's Neural Machine Translation System
* Word embeddings trained on Wikipedia using FastText were released recently by Facebook
* FastText Word Embeddings for Arabic were trained on the Arabic wikipedia corpus - vocabulary size = 610978

## Week 3
* Ran a pretrained German to English OpenNMT model. This does not seem viable for the following reasons - 
1. Many of the words encountered at test time are marked as unknown as they haven't been encountered during training time.[Sample Output](https://github.com/cibi29/Weekly-Status-Update/blob/master/results.txt)
2. Translations take approximately 40 minutes for every 750 sentences - (approximately 7000 words). 
3. Training the model again would require huge resources as well as time. 
* Therefore queried Google Translate with German Corpus of Patent Information and obtained the following results - 
1. Word2vec results on part and whole of currently translated data. Results seem to favourably show that word2vec accuracy improves with more machine translated training data. - [Graph](https://github.com/cibi29/Weekly-Status-Update/blob/master/g_translate_results.png)
2. Machine Translated Word2vec results vs original word2vec results. The results obtained are close to that of using half the enwik8 dataset. The vocabulary of machine translated training data is however lower - [Graph](https://github.com/cibi29/Weekly-Status-Update/blob/master/figure_1.png)

## Week 4
* Generated more translated german data and ran word2vec on them - Training data is approximately doubled from last week. 
1. Accuracy improves by only 2 percent. Final Accuracy : 17.3 percent
2. Training document size : 15101507 words.  Vocabulary Size : 24174
3. Accuracy observably improves with number of words in the vocabulary but the size of training data however contributes very little to increase in performance. 
4. Training Data, Vocab Size vs Accuracy - [Spreadsheet](https://docs.google.com/spreadsheets/d/1M5-BnB-KgTU_q1Ld6e8_NayMAwLYuaveREOSlJKF7g0/edit?usp=sharing) 
* Started two courses - one on NLP and another on Probability Theory  

## Week 5


* Read the following papers related to Evaluation of Word Embeddings
1. Evaluating Word Embeddings Using a Representative Suite of Practical Tasks - [Paper](https://cs.stanford.edu/~angeli/papers/2016-acl-veceval.pdf)
2. Evaluation methods for unsupervised word embeddings - [Paper](http://www.aclweb.org/anthology/D15-1036)
3. Community Evaluation and Exchange of Word Vectors - [Paper](http://www.manaalfaruqui.com/papers/acl14-vecdemo.pdf)
4. Intrinsic Evaluation of Word Vectors Fails to Predict Extrinsic Performance - [Paper](https://www.aclweb.org/anthology/W/W16/W16-2501.pdf)
