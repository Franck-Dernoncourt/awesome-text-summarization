# awesome-text-summarization

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of resources dedicated to text summarization

## Table of Contents

- [awesome-text-summarization](#awesome-text-summarization)
  - [Table of Contents](#table-of-contents)
  - [Contents](#contents)
    - [Corpus](#corpus)
    - [Text Summarization Software](#text-summarization-software)
    - [Word Representations](#word-representations)
      - [Word Representations for Chinese](#word-representations-for-chinese)
      - [Evaluation of Word Embeddings](#evaluation-of-word-embeddings)
      - [Evaluation of Word Embeddings for Chinese](#evaluation-of-word-embeddings-for-chinese)
    - [Sentence Representations](#sentence-representations)
      - [Evaluation of Sentence Embeddings](#evaluation-of-sentence-embeddings)
      - [Cross-lingual Sentence Representations](#cross-lingual-sentence-representations)
      - [Evaluation of Cross-lingual Sentence Representations](#evaluation-of-cross-lingual-sentence-representations)
    - [Language Representations](#language-representations)
      - [Cross-lingual Language Representations](#cross-lingual-language-representations)
    - [Extractive Text Summarization](#extractive-text-summarization)
    - [Abstractive Text Summarization](#abstractive-text-summarization)
    - [Text Summarization](#text-summarization)
    - [Chinese Text Summarization](#chinese-text-summarization)
    - [Program Source Code Summarization](#program-source-code-summarization)
    - [Entity Summarization](#entity-summarization)
    - [Evaluation Metrics](#evaluation-metrics)
    - [Opinion Summarization](#opinion-summarization)

## Contents

### Corpus

1. [Opinosis dataset](http://kavita-ganesan.com/opinosis-opinion-dataset) contains 51 articles. Each article is about a product’s feature, like iPod’s Battery Life, etc. and is a collection of reviews by customers who purchased that product. Each article in the dataset has 5 manually written “gold” summaries. Usually the 5 gold summaries are different but they can also be the same text repeated 5 times.
2. [Past DUC Data](https://www-nlpir.nist.gov/projects/duc/data.html) and [TAC Data](https://tac.nist.gov/data/index.html) include summarization data.
3. [English Gigaword](https://catalog.ldc.upenn.edu/LDC2003T05): English Gigaword was produced by Linguistic Data Consortium (LDC).
4. [Large Scale Chinese Short Text Summarization Dataset (LCSTS)](http://icrc.hitsz.edu.cn/Article/show/139.html): This corpus is constructed from the Chinese microblogging website SinaWeibo. It consists of over 2 million real Chinese short texts with short summaries given by the writer of each text.
5. Ziqiang Cao, Chengyao Chen, Wenjie Li, Sujian Li, Furu Wei, Ming Zhou. [TGSum: Build Tweet Guided Multi-Document Summarization Dataset](https://arxiv.org/abs/1511.08417v1). arXiv:1511.08417, 2015.
6. [scisumm-corpus](https://github.com/WING-NUS/scisumm-corpus) contains a release of the scientific document summarization corpus and annotations from the WING NUS group.
7. Avinesh P.V.S., Maxime Peyrard, Christian M. Meyer. [Live Blog Corpus for Summarization](https://arxiv.org/abs/1802.09884v1). arXiv:1802.09884, 2018.
8. Alexander R. Fabbri, Irene Li, Prawat Trairatvorakul, Yijiao He, Wei Tai Ting, Robert Tung, Caitlin Westerfield, Dragomir R. Radev.[TutorialBank: A Manually-Collected Corpus for Prerequisite Chains, Survey Extraction and Resource Recommendation](https://arxiv.org/abs/1805.04617). arXiv:1805.04617, 2018. The source code is [TutorialBank](https://github.com/Yale-LILY/TutorialBank). All the datasets could be found through the [search engine](http://tangra.cs.yale.edu/newaan/). The blog [TutorialBank: Learning NLP Made Easier](https://alex-fabbri.github.io/TutorialBank/) is an excellent user guide with step by step instructions on how to use the search engine.
9. [Legal Case Reports Data Set](https://archive.ics.uci.edu/ml/datasets/Legal+Case+Reports) contains Australian legal cases from the Federal Court of Australia (FCA).
10. [TIPSTER Text Summarization Evaluation Conference (SUMMAC)](https://www-nlpir.nist.gov/related_projects/tipster_summac/cmp_lg.html)  includes 183 documents.
11. [NEWS SUMMARY](https://www.kaggle.com/sunnysai12345/news-summary) consists of 4515 examples.
12. [BBC News Summary](https://www.kaggle.com/pariza/bbc-news-summary/data) consists of 417 political news articles of BBC from 2004 to 2005.
13. CNN / Daily Mail dataset (non-anonymized) for summarization is produced by the code [cnn-dailymail](https://github.com/abisee/cnn-dailymail).
14. [sentence-compression](https://github.com/google-research-datasets/sentence-compression) is a large corpus of uncompressed and compressed sentences from news articles. The algorithm to collect the data is described here: [Overcoming the Lack of Parallel Data in Sentence Compression](http://www.aclweb.org/anthology/D/D13/D13-1155.pdf) by Katja Filippova and Yasemin Altun, EMNLP '13.
15. [The Columbia Summarization Corpus (CSC)](https://www.cs.ucsb.edu/~william/papers/ijcnlp2011.pdf) was retrieved from the output of the [Newsblaster online news summarization system](http://newsblaster.cs.columbia.edu/) that crawls the Web for news articles, clusters them on specific topics and produces multidocument summaries for each cluster. They collected a total of 166,435 summaries containing 2.5 million sentences and covering 2,129 days in the 2003-2011 period. Additional references of the Columbia Newsblaster summarizer can be found on the website of [Columbia NLP group publication page](http://www1.cs.columbia.edu/nlp/papers.cgi).
16. [WikiHow-Dataset](https://github.com/mahnazkoupaee/WikiHow-Dataset)  a new large-scale dataset using the online [WikiHow] (http://www.wikihow.com) knowledge base. Each article consists of multiple paragraphs and each paragraph starts with a sentence summarizing it. By merging the paragraphs to form the article and the paragraph outlines to form the summary, the resulting version of the dataset contains more than 200,000 long-sequence pairs.
17. Guy Lev, Michal Shmueli-Scheuer, Jonathan Herzig, Achiya Jerbi, David Konopnicki. [TalkSumm: A Dataset and Scalable Annotation Method for Scientific Paper Summarization Based on Conference Talks](https://arxiv.org/abs/1906.01351v2). arXiv:1906.01351v2, ACL 2019.
1. Diego Antognini, Boi Faltings. [GameWikiSum: a Novel Large Multi-Document Summarization Dataset](https://arxiv.org/abs/2002.06851v1). arXiv:2002.06851v1, 2020. The data is available [here](http://lia.epfl.ch/Datasets/Full_GameWiki.zip).
1. Canwen Xu, Jiaxin Pei, Hongtao Wu, Yiyu Liu, Chenliang Li. [MATINF: A Jointly Labeled Large-Scale Dataset for Classification, Question Answering and Summarization](https://arxiv.org/abs/2004.12302v2). arXiv:2004.12302v2, ACL 2020.
1. Thomas Scialom, Paul-Alexis Dray, Sylvain Lamprier, Benjamin Piwowarski, Jacopo Staiano. [MLSUM: The Multilingual Summarization Corpus](https://arxiv.org/abs/2004.14900v1). arXiv:2004.14900v1, 2020.
1. Max Savery, Asma Ben Abacha, Soumya Gayen, Dina Demner-Fushman. [Question-Driven Summarization of Answers to Consumer Health Questions](https://arxiv.org/abs/2005.09067v2). arXiv:2005.09067v2, 2020.
1. Demian Gholipour Ghalandari, Chris Hokamp, Nghia The Pham, John Glover, Georgiana Ifrim. [A Large-Scale Multi-Document Summarization Dataset from the Wikipedia Current Events Portal](https://arxiv.org/abs/2005.10070v1). arXiv:2005.10070v1, 2020.


### Text Summarization Software

1. [sumeval](https://github.com/chakki-works/sumeval) implemented in Python is a well tested & multi-language evaluation framework for text summarization.
2. [sumy](https://github.com/miso-belica/sumy) is a simple library and command line utility for extracting summary from HTML pages or plain texts. The package also contains simple evaluation framework for text summaries. Implemented summarization methods are *Luhn*, *Edmundson*, *LSA*, *LexRank*, *TextRank*, *SumBasic* and *KL-Sum*.
3. [TextRank4ZH](https://github.com/letiantian/TextRank4ZH) implements the *TextRank* algorithm to extract key words/phrases and text summarization
in Chinese. It is written in Python.
4. [snownlp](https://github.com/isnowfy/snownlp) is python library for processing Chinese text.
5. [PKUSUMSUM](https://github.com/PKULCWM/PKUSUMSUM) is an integrated toolkit for automatic document summarization. It supports single-document, multi-document and topic-focused multi-document summarizations, and a variety of summarization methods have been implemented in the toolkit. It supports Western languages (e.g. English) and Chinese language.
6. [fnlp](https://github.com/FudanNLP/fnlp) is a toolkit for Chinese natural language processing.
7. [fairseq](https://github.com/pytorch/fairseq) is a sequence modeling toolkit that allows researchers and developers to train custom models for translation, summarization, language modeling and other text generation tasks. It provides reference implementations of various sequence-to-sequence model.
8. [paperswithcode](https://paperswithcode.com/area/natural-language-processing/text-summarization) a website that collects research
papers in computer science with together with their code artifacts,
this link is to so a section on natural language texts summarization.
9. [CX_DB8](https://github.com/Hellisotherpeople/CX_DB8) a modern queryable summarizer utilizing the latest in pre-trained language models.

### Word Representations

1. G. E. Hinton, J. L, McClelland, and D. E. Rumelhart. [Distributed representations](https://web.stanford.edu/~jlmcc/papers/PDP/Chapter3.pdf). In D. E. Rumelhart and J. L. McClelland, Parallel Distributed Processing: Explorations in the Microstructure of Cognition. Volume 1: Foundations, MIT Press, Cambridge, MA. 1986. The related slides are [here](http://www.cs.toronto.edu/~bonner/courses/2014s/csc321/lectures/lec5.pdf) or [here](http://www.cs.toronto.edu/~bonner/courses/2016s/csc321/lectures/extra/coarse.pdf).
   * "Distributed representation" means a many-tomany relationship between two types of representation (such as concepts and neurons): 1. Each concept is represented by many
   neurons; 2. Each neuron participates in the representation of many concepts.
2. [Language Modeling with N-Grams](https://web.stanford.edu/~jurafsky/slp3/4.pdf). The related slides are [here](https://web.stanford.edu/~jurafsky/slp3/slides/LM_4.pptx). It introduced language modeling and the N-gram, one of the most widely used tools in language processing.
   * Language models offer a way to assign a probability to a sentence or other sequence of words, and to predict a word from preceding words.
   * N-grams are Markov models that estimate words from a fixed window of previous words. N-gram probabilities can be estimated by counting in a corpus and normalizing (the maximum likelihood estimate).
   * N-gram language models are evaluated extrinsically in some task, or intrinsically using perplexity.
   * The perplexity of a test set according to a language model is the geometric mean of the inverse test set probability computed by the model.
   * Smoothing algorithms provide a more sophisticated way to estimat the probability of N-grams. Commonly used smoothing algorithms for N-grams rely on lower-order N-gram counts through backoff or interpolation.
   * There are at least two drawbacks for the n-gram language model. First, it is not taking into account contexts farther than 1 or 2 words. N-grams with n up to 5 (i.e. 4 words of context) have been reported, though, but due to data scarcity, most predictions are made with a much shorter context. Second, it is not taking into account the “similarity” between words. 
3. Yoshua Bengio, Réjean Ducharme, Pascal Vincent and Christian Jauvin. [A Neural Probabilistic Language Model](http://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf). Journal of Machine Learning Research, 2003.
   - They propose continuous space LMs using neural networks to fight the curse of dimensionality by learning a distributed representation for words.
   - The model learns simultaneously (1) a distributed representation for each word along with (2) the probability function for word sequences, expressed in terms of these representations.
   - Generalization is obtained because a sequence of words that has never been seen before gets high probability if it is made of words that are similar (in the sense of having a nearby representation) to words forming an already seen sentence.
   - The idea of the proposed approach can be summarized: 1. associate with each word in the vocabulary a distributed word feature vector, 2. express the joint probability function of word sequences in terms of the feature vectors of these words in the sequence, and 3. learn simultaneously the word feature vectors and the parameters of that probability function.
4. In the following two papers, it is shown that both to project all words of the context onto a continuous space and calculate the language model probability for the given context can be performed by a neural network using two hidden layers.
   * Holger Schwenk and Jean-Luc Gauvain. [Training Neural Network Language Models On Very Large Corpora](ftp://tlp.limsi.fr/public/emnlp05.pdf). in Proc. Joint Conference HLT/EMNLP, 2005.
   * Holger Schwenk. [Continuous space language models](https://wiki.inf.ed.ac.uk/twiki/pub/CSTR/ListenSemester2_2009_10/sdarticle.pdf). Computer Speech and Language, 2007.
5. Tomas Mikolov's series of papers improved the quality of word representations:
   * T. Mikolov, J. Kopecky, L. Burget, O. Glembek and J. Cernocky. [Neural network based language models for higly inflective languages](http://www.fit.vutbr.cz/research/groups/speech/publi/2009/mikolov_ic2009_nnlm_4.pdf). Proc. ICASSP, 2009. The first step in their architecture is training of bigram neural network: given word w from vocabulary V, estimate probability distribution of the next word in text. To compute projection of word w onto a  continuous space, half of the bigram network (first two layers) is used to compute values in hidden layer. Values from the hidden layer of bigram network are used to form input layer of n-gram network.
   * T. Mikolov, W.T. Yih and G. Zweig. [Linguistic Regularities in Continuous Space Word Representations](https://www.aclweb.org/anthology/N13-1090). NAACL HLT, 2013. They examine the vector-space word representations that are implicitly learned by the input-layer weights. They find that these representations are surprisingly good at capturing syntactic and semantic regularities in language, and that each relationship is characterized by a relation-specific vector offset. This allows vector-oriented reasoning based on the offsets between words. Remarkably, this method outperforms the best previous systems.
   * Tomas Mikolov, Kai Chen, Greg Corrado and Jeffrey Dean. [Efficient Estimation of Word Representations in Vector Space](https://arxiv.org/abs/1301.3781v3). arXiv:1301.3781v3, 2013. They propose two new model architectures for learning distributed representations: 1. Continuous Bag-of-Words Model (CBOW) builds a log-linear classifier with context words at the input, where the training criterion is to correctly classify the current word; 2. Continuous Skip-gram Model uses each current word as an input to a log-linear classifier with continuous projection layer, and predicts words within a certain range before and after the current word.
   * Tomas Mikolov, Ilya Sutskever, Kai Chen, Greg Corrado and Jeffrey Dean. [Distributed Representations of Words and Phrases and their Compositionality](https://arxiv.org/abs/1310.4546). arXiv:1310.4546, 2013. The source code written in C is [word2vec](https://github.com/tmikolov/word2vec). They present several extensions of the original Skip-gram model. They show that sub-sampling of frequent words during training results in a significant speedup (around 2x - 10x), and improves accuracy of the representations of less frequent words. In addition, they present a simplified variant of Noise Contrastive Estimation for training the Skip-gram model that results in faster training and better vector representations for frequent words. Word based model is extended to phrase based model. They found that simple vector addition can often produce meaningful results.
   * Tomas Mikolov, Edouard Grave, Piotr Bojanowski, Christian Puhrsch and Armand Joulin.[Advances in Pre-Training Distributed Word Representations](https://arxiv.org/abs/1712.09405). arXiv:1712.09405, 2017. They show that several modifications of the standard word2vec training pipeline significantly improves the quality of the resulting word vectors: position-dependent weighting, the phrase representations and the subword information.
6. Christopher Olah. [Deep Learning, NLP, and Representations](http://colah.github.io/posts/2014-07-NLP-RNNs-Representations/). This post reviews some extremely remarkable results in applying deep neural networks to NLP, where the representation perspective of deep learning is a powerful view that seems to answer why deep neural networks are so effective. 
7. Levy, Omer, and Yoav Goldberg. [Neural word embedding as implicit matrix factorization](https://papers.nips.cc/paper/5477-neural-word-embedding-as-implicit-matrix-factorization.pdf). NIPS. 2014.
8. [Sanjeev Arora](http://www.offconvex.org/)'s a series of blogs/papers about word embeddings:
   * The blog [Semantic Word Embeddings](http://www.offconvex.org/2015/12/12/word-embeddings-1/) is a very good overview about word embedding.
   * The blog [Word Embeddings: Explaining their properties](http://www.offconvex.org/2016/02/14/word-embeddings-2/) introduces the main result about [RAND-WALK: A Latent Variable Model Approach to Word Embeddings](https://arxiv.org/abs/1502.03520), which answers three interesting questions: 1. Why do low-dimensional embeddings capture huge statistical information? 2. Why do low dimensional embeddings work better than high-dimensional ones? 3. Why do Semantic Relations correspond to Directions?
   * The blog [Linear algebraic structure of word meanings](http://www.offconvex.org/2016/07/10/embeddingspolysemy/) introduces the main result about [Linear Algebraic Structure of Word Senses, with Applications to Polysemy](https://arxiv.org/abs/1601.03764), which shows that word senses are easily accessible in many current word embeddings.
9. [Word2Vec Resources](http://mccormickml.com/2016/04/27/word2vec-resources/): This is a post with links to and descriptions of word2vec tutorials, papers, and implementations.
10. [Word embeddings: how to transform text into numbers](https://monkeylearn.com/blog/word-embeddings-transform-text-numbers/)
11. [GloVe: Global Vectors for Word Representation](https://nlp.stanford.edu/projects/glove/) an unsupervised learning algorithm for obtaining vector representations for words. Training is performed on aggregated global word-word co-occurrence statistics from a corpus.
12. Li, Yitan, et al. [Word embedding revisited: A new representation learning and explicit matrix factorization perspective](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.719.9973&rep=rep1&type=pdf). IJCAI. 2015.
13. O. Levy, Y. Goldberg, and I. Dagan. [Improving Distributional Similarity with Lessons Learned from Word Embeddings](http://www.aclweb.org/anthology/Q15-1016). Trans. Assoc. Comput. Linguist., 2015.
14. Eric Nalisnick, Sachin Ravi. [Learning the Dimensionality of Word Embeddings](https://arxiv.org/abs/1511.05392v3). arXiv:1511.05392, 2015.
    * They describe a method for learning word embeddings with data-dependent dimensionality. Their Stochastic Dimensionality Skip-Gram (SD-SG) and Stochastic Dimensionality Continuous Bag-of-Words (SD-CBOW) are nonparametric analogs of Mikolov et al.'s (2013) well-known 'word2vec' model.
15. William L. Hamilton, Jure Leskovec, Dan Jurafsky. [Diachronic Word Embeddings Reveal Statistical Laws of Semantic Change](https://aclanthology.info/pdf/P/P16/P16-1141.pdf).
    * Hamilton et al. model changes in word meaning by fitting word embeddings on consecutive corpora of historical language. They compare several ways of quantifying meaning (co-occurrence vectors weighted by PPMI, SVD embeddings and word2vec embeddings), and align historical embeddings from different corpora by finding the optimal rotational alignment that preserves the cosine similarities as much as possible.
16. Zijun Yao, Yifan Sun, Weicong Ding, Nikhil Rao, Hui Xiong. [Dynamic Word Embeddings for Evolving Semantic Discovery](https://arxiv.org/abs/1703.00607). arXiv:1703.00607v2, International Conference on Web Search and Data Mining (WSDM 2018).
17. Yang, Wei  and  Lu, Wei  and  Zheng, Vincent. [A Simple Regularization-based Algorithm for Learning Cross-Domain Word Embeddings](http://www.aclweb.org/anthology/D/D17/D17-1312.pdf). ACL, 2017. The source code in C is [cross_domain_embedding](https://github.com/Victor0118/cross_domain_embedding).
    - This paper presents a simple yet effective method for learning word embeddings based on text from different domains.
18. Sebastian Ruder. [Word embeddings in 2017: Trends and future directions](http://ruder.io/word-embeddings-2017/)
19. Bryan McCann, James Bradbury, Caiming Xiong and Richard Socher. [Learned in Translation: Contextualized Word Vectors](https://arxiv.org/abs/1708.00107). For a high-level overview of why CoVe are great, check out the [post](https://einstein.ai/research/learned-in-translation-contextualized-word-vectors). 
    * A Keras/TensorFlow implementation of the MT-LSTM/CoVe is [CoVe](https://github.com/rgsachin/CoVe).
    * A PyTorch implementation of the MT-LSTM/CoVe is [cove](https://github.com/salesforce/cove).
20. Maria Pelevina, Nikolay Arefyev, Chris Biemann, Alexander Panchenko. [Making Sense of Word Embeddings](https://arxiv.org/abs/1708.03390). arXiv:1708.03390, 2017. The source code written in Python is [sensegram](https://github.com/tudarmstadt-lt/sensegram).
    - Making sense embedding out of word embeddings using graph-based word sense induction.
21. Piotr Bojanowski, Edouard Grave, Armand Joulin, Tomas Mikolov. [Enriching Word Vectors with Subword Information](https://arxiv.org/abs/1607.04606v2). arXiv:1607.04606v2, 2017. The souce code in C++11 is [fastText](https://fasttext.cc/), which is a library for efficient learning of word representations and sentence classification.
    * They propose a new approach based on the skipgram model, where each word is represented as a bag of character n-grams. A vector representation is associated to each character n-gram; words being represented as the sum of these representations. 
22. Alexis Conneau, Guillaume Lample, Marc'Aurelio Ranzato, Ludovic Denoyer and Herv{\'e} J{\'e}gou. [Word Translation Without Parallel Data](https://arxiv.org/abs/1710.04087). arXiv:1710.04087, 2017. The source code in Python is [MUSE](https://github.com/facebookresearch/MUSE), which is a library for multilingual unsupervised or supervised word embeddings.
23. Gabriel Grand, Idan Asher Blank, Francisco Pereira, Evelina Fedorenko. [Semantic projection: recovering human knowledge of multiple, distinct object features from word embeddings](https://arxiv.org/abs/1802.01241v2). arXiv:1802.01241, 2018.
    * Could context-dependent relationships be recovered from word embeddings? To address this issue, they introduce a powerful, domain-general solution: "semantic projection" of word-vectors onto lines that represent various object features, like size (the line extending from the word "small" to "big"), intelligence (from "dumb" to "smart"), or danger (from "safe" to "dangerous").
25. Edouard Grave, Piotr Bojanowski, Prakhar Gupta, Armand Joulin, Tomas Mikolov. [Learning Word Vectors for 157 Languages](https://arxiv.org/abs/1802.06893v2). arXiv:1802.06893v2, Proceedings of LREC, 2018.
    * They describe how high quality word representations for 157 languages are trained. They used two sources of data to train these models: the free online encyclopedia Wikipedia and data from the common crawl project. Pre-trained word vectors for 157 languages are [available](https://fasttext.cc/docs/en/crawl-vectors.html).
26. Douwe Kiela, Changhan Wang and Kyunghyun Cho. [Context-Attentive Embeddings for Improved Sentence Representations](https://arxiv.org/abs/1804.07983). arXiv:1804.07983, 2018. 
    * While one of the first steps in many NLP systems is selecting what embeddings to use, they argue that such a step is better left for neural networks to figure out by themselves. To that end, they introduce a novel, straightforward yet highly effective method for combining multiple types of word embeddings in a single model, leading to state-of-the-art performance within the same model class on a variety of tasks.
27. Laura Wendlandt, Jonathan K. Kummerfeld, Rada Mihalcea. [Factors Influencing the Surprising Instability of Word Embeddings](https://arxiv.org/abs/1804.09692v1). arXiv:1804.09692, NAACL HLT 2018.
    * They provide empirical evidence for how various factors contribute to the stability of word embeddings, and analyze the effects of stability on downstream tasks.
28. [magnitude](https://github.com/plasticityai/magnitude) is a feature-packed Python package and vector storage file format for utilizing vector embeddings in machine learning models in a fast, efficient, and simple manner.
29. Jose Camacho-Collados, Mohammad Taher Pilehvar. [From Word to Sense Embeddings: A Survey on Vector Representations of Meaning](https://arxiv.org/abs/1805.04032v3). arXiv:1805.04032v3, 2018. 

#### Word Representations for Chinese

1. X. Chen, L.  Xu, Z.  Liu, M. Sun and H. Luan. [Joint Learning of Character and Word Embeddings](http://nlp.csai.tsinghua.edu.cn/~lzy/publications/ijcai2015_character.pdf). IJCAI, 2015. The source code in C is [CWE](https://github.com/Leonard-Xu/CWE).
2. Jian Xu, Jiawei Liu, Liangang Zhang, Zhengyu Li, Huanhuan Chen. [Improve Chinese Word Embeddings by Exploiting Internal Structure](http://www.aclweb.org/anthology/N16-1119). NAACL 2016. The source code in C is [SCWE](https://github.com/JianXu123/SCWE).
3. Jinxing Yu, Xun Jian, Hao Xin and Yangqiu Song. [Joint Embeddings of Chinese Words, Characters, and Fine-grained Subcharacter Components](http://www.cse.ust.hk/~yqsong/papers/2017-EMNLP-ChineseEmbedding.pdf). EMNLP, 2017. The source code in C is [JWE](https://github.com/HKUST-KnowComp/JWE).
4. Shaosheng Cao and Wei Lu. [Improving Word Embeddings with Convolutional Feature Learning and Subword Information](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/viewPDFInterstitial/14724/14187). AAAI, 2017. The source code in C# is [IWE](https://github.com/ShelsonCao/IWE).
5. Zhe Zhao, Tao Liu, Shen Li, Bofang Li and Xiaoyong Du. [Ngram2vec: Learning Improved Word Representations from Ngram Co-occurrence Statistics](http://aclweb.org/anthology/D17-1023).  EMNLP, 2017. The source code in Python is [ngram2vec](https://github.com/zhezhaoa/ngram2vec).
6. Shaosheng Cao, Wei Lu, Jun Zhou, Xiaolong Li. [cw2vec: Learning Chinese Word Embeddings with Stroke n-gram Information](https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/view/17444). AAAI, 2018. The source code in C++ is [cw2vec](https://github.com/bamtercelboo/cw2vec). 

#### Evaluation of Word Embeddings

1. Tobias Schnabel, Igor Labutov, David Mimno and Thorsten Joachims. [Evaluation methods for unsupervised word embeddings](https://www.cs.cornell.edu/~schnabts/downloads/schnabel2015embeddings.pdf). EMNLP, 2015. The slides are [here](https://www.cs.cornell.edu/~schnabts/downloads/slides/schnabel2015eval.pdf).
2. Billy Chiu, Anna Korhonen and  Sampo Pyysalo. [Intrinsic Evaluation of Word Vectors Fails to Predict Extrinsic Performance](https://www.aclweb.org/anthology/W/W16/W16-2501.pdf). Proceedings of the 1st Workshop on Evaluating Vector-Space Rep- resentations for NLP, 2016.
2. Stanisław Jastrzebski, Damian Leśniak, Wojciech Marian Czarnecki. [How to evaluate word embeddings? On importance of data efficiency and simple supervised tasks](https://arxiv.org/abs/1702.02170). arXiv:1702.02170, 2017. The source code in Python is [word-embeddings-benchmarks](https://github.com/kudkudak/word-embeddings-benchmarks).
3. Amir Bakarov. [A Survey of Word Embeddings Evaluation Methods](https://arxiv.org/abs/1801.09536). arXiv:1801.09536, 2018.

#### Evaluation of Word Embeddings for Chinese

1. Shen Li, Zhe Zhao, Renfen Hu, Wensi Li, Tao Liu, Xiaoyong Du. [Analogical Reasoning on Chinese Morphological and Semantic Relations](https://arxiv.org/abs/1805.06504). arXiv:1805.06504, ACL, 2018. 
   * The project [Chinese-Word-Vectors](https://github.com/Embedding/Chinese-Word-Vectors) provides 100+ Chinese Word Embeddings trained with different representations (dense and sparse), context features (word, ngram, character, and more), and corpora. Moreover, it provides a Chinese analogical reasoning dataset CA8 and an evaluation toolkit for users to evaluate the quality of their word vectors.
2. Yuanyuan Qiu, Hongzheng Li, Shen Li, Yingdi Jiang, Renfen Hu, Lijiao Yang. [Revisiting Correlations between Intrinsic and Extrinsic Evaluations of Word Embeddings](http://www.cips-cl.org/static/anthology/CCL-2018/CCL-18-086.pdf). Chinese Computational Linguistics and Natural Language Processing Based on Naturally Annotated Big Data, 2018.


### Sentence Representations

1. Kalchbrenner, Nal, Edward Grefenstette, and Phil Blunsom. [A convolutional neural network for modelling sentences](http://arxiv.org/abs/1404.2188). arXiv:1404.2188, 2014.
2. Quoc Le and Tomas Mikolov. [Distributed representations of sentences and documents](https://arxiv.org/abs/1405.4053v2). arXiv:1405.4053v2, 2014.
   * Distributed Memory Model of Paragraph Vectors (PV-DM): The inspiration is that the paragraph vectors are asked to contribute to the prediction task of the next word given many contexts sampled from the paragraph.  The paragraph vector and word vectors are averaged or concatenated to predict the next word in a context. The contexts are fixed-length and sampled from a sliding window over the paragraph. The paragraph vector is shared across all contexts generated from the same paragraph but not across paragraphs. However, the word vector matrix is shared across paragraphs. The downside is at prediction time, inference needs to be performed to compute a new vector.
   * Distributed Bag of Words version of Paragraph Vector (PV-DBOW): This modle is to ignore the context words in the input, but force the model to predict words randomly sampled from the paragraph in the output.
3. Yoon Kim. [Convolutional neural networks for sentence classification](http://arxiv.org/abs/1408.5882). arXiv:1408.5882, EMNLP 2014.
4. Ryan Kiros, Yukun Zhu, Ruslan Salakhutdinov, Richard S. Zemel, Antonio Torralba, Raquel Urtasun and Sanja Fidler. [Skip-Thought Vectors](https://arxiv.org/abs/1506.06726). arXiv:1506.06726, 2015. The source code in Python is [skip-thoughts](https://github.com/ryankiros/skip-thoughts). The TensorFlow implementation of *Skip-Thought Vectors* is [skip_thoughts](https://github.com/tensorflow/models/tree/master/research/skip_thoughts)
   * Instead of using a word to predict its surrounding context, they instead encode a sentence to predict the sentences around it. The skip-thoughts is in the framework of encoder-decoder models: an encoder maps words to a sentence vector and a decoder is used to generate the surrounding sentences.
   * The end product of skip-thoughts is the encoder,  which can then be used to generate fixed length representations of sentences. The decoders are thrown away after training.
   * A good tutorial to this paper is [My Thoughts On Skip Thoughts](http://sanyam5.github.io/my-thoughts-on-skip-thoughts/).
5. Andrew M. Dai, Quoc V. Le. [Semi-supervised Sequence Learning](https://arxiv.org/abs/1511.01432). arXiv:1511.01432, 2015.
   - They present two approaches that use unlabeled data to improve sequence learning with recurrent networks. The first approach is to predict what comes next in a sequence, which is a conventional language model in natural language processing. The second approach is to use a sequence autoencoder, which reads the input sequence into a vector and predicts the input sequence again. These two algorithms can be used as a "pretraining" step for a later supervised sequence learning algorithm.
   - Their semi-supervised learning approach is related to Skip-Thought vectors with two differences. The first difference is that Skip-Thought is a harder objective, because it predicts adjacent sentences. The second is that Skip-Thought is a pure unsupervised learning algorithm, without fine-tuning.
6. John Wieting and Mohit Bansal and Kevin Gimpel and Karen Livescu. [Towards Universal Paraphrastic Sentence Embeddings](https://arxiv.org/abs/1511.08198). arXiv:1511.08198, ICLR 2016. The source code written in Python is [iclr2016](https://github.com/jwieting/iclr2016).
7. Zhe Gan, Yunchen Pu, Ricardo Henao, Chunyuan Li, Xiaodong He, Lawrence Carin. [Learning Generic Sentence Representations Using Convolutional Neural Networks](https://arxiv.org/abs/1611.07897). arXiv:1611.07897, EMNLP 2017. The training code written in Python is [ConvSent](https://github.com/zhegan27/ConvSent).
8. Matteo Pagliardini, Prakhar Gupta, Martin Jaggi. [Unsupervised Learning of Sentence Embeddings using Compositional n-Gram Features](https://arxiv.org/abs/1703.02507v2). arXiv:1703.02507, NAACL 2018. The source code in Python is [sent2vec](https://github.com/epfml/sent2vec). 
9. Zhouhan Lin, Minwei Feng, Cicero Nogueira dos Santos, Mo Yu, Bing Xiang, Bowen Zhou, Yoshua Bengio. [A Structured Self-attentive Sentence Embedding](https://arxiv.org/abs/1703.03130). arXiv:1703.03130, ICLR 2017.
10. Ledell Wu, Adam Fisch, Sumit Chopra, Keith Adams, Antoine Bordes, Jason Weston. [StarSpace: Embed All The Things](https://arxiv.org/abs/1709.03856v5). arXiv:1709.03856v5, 2017. The source code in C++11 is [StarSpace](https://github.com/facebookresearch/Starspace/).
11. Alexis Conneau, Douwe Kiela, Holger Schwenk, Loic Barrault, Antoine Bordes. [Supervised Learning of Universal Sentence Representations from Natural Language Inference Data](https://arxiv.org/abs/1705.02364v5). arXiv:1705.02364v5, EMNLP 2017. The source code in Python is [InferSent](https://github.com/facebookresearch/InferSent).
12. Sanjeev Arora, Yingyu Liang, Tengyu Ma. [A Simple but Tough-to-Beat Baseline for Sentence Embeddings](https://openreview.net/pdf?id=SyK00v5xx). ICLR 2017. The source code written in Python is [SIF](https://github.com/PrincetonML/SIF). [SIF_mini_demo](https://github.com/PrincetonML/SIF_mini_demo) is a minimum example for the sentence embedding algorithm. [sentence2vec](https://github.com/peter3125/sentence2vec) is another implementation.
    - A weighted average of words by their distance from the first principal component of a sentence is proposed, which  yields a remarkably robust approximate sentence vector embedding.
    - However, this “smooth inverse frequency” approach comes with limitations. Not only is calculating PCA for every sentence in a document computationally complex, but the first principal component of a small number of normally distributed words in a high dimensional space is subject to random fluctuation. Their calculation of word frequencies from the unigram count of the word in the corpus also means that their approach still does not work for out-of-vocab words, has no equivalent in other vector spaces and can’t be generated from the word vectors alone.
13. Yixin Nie, Mohit Bansal. [Shortcut-Stacked Sentence Encoders for Multi-Domain Inference](https://arxiv.org/abs/1708.02312). arXiv:1708.02312, EMNLP 2017. The source code in Python is [multiNLI_encoder](https://github.com/easonnie/multiNLI_encoder). The new repo [ResEncoder]( https://github.com/easonnie/ResEncoder) is for Residual-connected sentence encoder for NLI.
14. Allen Nie, Erin D. Bennett, Noah D. Goodman. [DisSent: Sentence Representation Learning from Explicit Discourse Relations](https://arxiv.org/abs/1710.04334v2). arXiv:1710.04334v2, 2018.
15. Andreas Rücklé, Steffen Eger, Maxime Peyrard, Iryna Gurevych. [Concatenated Power Mean Word Embeddings as Universal Cross-Lingual Sentence Representations](https://arxiv.org/abs/1803.01400v2).  arXiv:1803.01400v2, 2018. The source code written in Python is [arxiv2018-xling-sentence-embeddings](https://github.com/UKPLab/arxiv2018-xling-sentence-embeddings).
16. Lajanugen Logeswaran, Honglak Lee. [An efficient framework for learning sentence representations](https://arxiv.org/abs/1803.02893). arXiv:1803.02893, ICLR 2018. The open review comments are listed [here](https://openreview.net/forum?id=rJvJXZb0W).
17. Eric Zelikman. [Context is Everything: Finding Meaning Statistically in Semantic Spaces](https://arxiv.org/abs/1803.08493). arXiv:1803.08493, 2018.
18. Daniel Cer, Yinfei Yang, Sheng-yi Kong, Nan Hua, Nicole Limtiaco, Rhomni St. John, Noah Constant, Mario Guajardo-Cespedes, Steve Yuan, Chris Tar, Yun-Hsuan Sung, Brian Strope, Ray Kurzweil. [Universal Sentence Encoder](https://arxiv.org/abs/1803.11175v2). arXiv:1803.11175v2, 2018.
19. Sandeep Subramanian, Adam Trischler, Yoshua Bengio, Christopher J Pal. [Learning General Purpose Distributed Sentence Representations via Large Scale Multi-task Learning](https://arxiv.org/abs/1804.00079). arXiv:1804.00079, ICLR 2018.
20. Nils Reimers, Iryna Gurevych. [Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks](https://arxiv.org/abs/1908.10084v1). arXiv:1908.10084v1, EMNLP 2019. This publication has been integrated into the framework [sentence-transformers](https://github.com/UKPLab/sentence-transformers), which provides an easy method to compute dense vector representations for sentences, paragraphs, and images.
21. Yan Zhang, Ruidan He, Zuozhu Liu, Kwan Hui Lim, Lidong Bing. [An Unsupervised Sentence Embedding Method by Mutual Information Maximization](https://arxiv.org/abs/2009.12061v2). arXiv:2009.12061v2, EMNLP 2020. 
22. Bohan Li, Hao Zhou, Junxian He, Mingxuan Wang, Yiming Yang, Lei Li. [On the Sentence Embeddings from Pre-trained Language Models](https://arxiv.org/abs/2011.05864v1). arXiv:2011.05864v1. The code is available at [BERT-flow](https://github.com/bohanli/BERT-flow). [IS-BERT](https://github.com/yanzhangnlp/IS-BERT) contains the code.
23. Tianyu Gao, Xingcheng Yao, Danqi Chen. [SimCSE: Simple Contrastive Learning of Sentence Embeddings](https://arxiv.org/abs/2104.08821v1). arXiv:2104.08821v1. [SimCSE](https://github.com/princeton-nlp/SimCSE) contains the code and pre-trained models for this model.
24. Kexin Wang, Nils Reimers, Iryna Gurevych. [TSDAE: Using Transformer-based Sequential Denoising Auto-Encoder for Unsupervised Sentence Embedding Learning](https://arxiv.org/abs/2104.06979v1). arXiv:2104.06979v1.

#### Evaluation of Sentence Embeddings

1. Yossi Adi, Einat Kermany, Yonatan Belinkov, Ofer Lavi, Yoav Goldberg. [Fine-grained Analysis of Sentence Embeddings Using Auxiliary Prediction Tasks](https://arxiv.org/abs/1608.04207v3). arXiv:1608.04207v3, 2017.
   * They define prediction tasks around isolated aspects of sentence structure (namely sentence length, word content, and word order), and score representations by the ability to train a classifier to solve each prediction task when using the representation as input.
2. Alexis Conneau, Douwe Kiela. [SentEval: An Evaluation Toolkit for Universal Sentence Representations](https://arxiv.org/abs/1803.05449). arXiv:1803.05449, LREC 2018. The source code in Python is [SentEval](https://github.com/facebookresearch/SentEval). **SentEval** encompasses a variety of tasks, including binary and multi-class classification, natural language inference and sentence similarity.
3. Alex Wang, Amapreet Singh, Julian Michael, Felix Hill, Omer Levy, Samuel R. Bowman. [GLUE: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding](https://arxiv.org/abs/1804.07461). arXiv:1804.07461, 2018.
4. Alexis Conneau, German Kruszewski, Guillaume Lample, Loïc Barrault, Marco Baroni. [What you can cram into a single vector: Probing sentence embeddings for linguistic properties](https://arxiv.org/abs/1805.01070v2). arXiv:1805.01070v2, 2018.
5. Christian S. Perone, Roberto Silveira, Thomas S. Paula. [Evaluation of sentence embeddings in downstream and linguistic probing tasks](https://arxiv.org/abs/1806.06259). arXiv:1806.06259, 2018.

#### Cross-lingual Sentence Representations

1. [LASER](https://github.com/facebookresearch/LASER) is a library to calculate multilingual sentence embeddings:
   - Holger Schwenk and Matthijs Douze. [Learning Joint Multilingual Sentence Representations with Neural Machine Translation](https://aclanthology.info/papers/W17-2619/w17-2619). ACL workshop on Representation Learning for NLP, 2017.
   - Holger Schwenk and Xian Li. [A Corpus for Multilingual Document Classification in Eight Languages](http://www.lrec-conf.org/proceedings/lrec2018/pdf/658.pdf).  LREC, 2018.
   - Holger Schwenk. [Filtering and Mining Parallel Data in a Joint Multilingual Space](https://arxiv.org/abs/1805.09822). arXiv:1805.09822, ACL, 2018.
   - Mikel Artetxe, Holger Schwenk. [Margin-based Parallel Corpus Mining with Multilingual Sentence Embeddings](https://arxiv.org/abs/1811.01136). arXiv:1811.01136, 2018.
   - Mikel Artetxe, Holger Schwenk. [Massively Multilingual Sentence Embeddings for Zero-Shot Cross-Lingual Transfer and Beyond](https://arxiv.org/abs/1812.10464). arXiv:1812.10464, 2018.
     - They learn a single, language agnostic BiLSTM shared encoder that can handle 93 different languages, which is coupled with an auxiliary decoder and trained over parallel corpora.

#### Evaluation of Cross-lingual Sentence Representations

1. Alexis Conneau, Guillaume Lample, Ruty Rinott, Adina Williams, Samuel R. Bowman, Holger Schwenk, Veselin Stoyanov. [XNLI: Evaluating Cross-lingual Sentence Representations](https://arxiv.org/abs/1809.05053). arXiv:1809.05053, EMNLP 2018.

### Language Representations

1. Jeremy Howard, Sebastian Ruder. [Universal Language Model Fine-tuning for Text Classification](https://arxiv.org/abs/1801.06146v5). arXiv:1801.06146v5, ACL 2018.
   * To address the lack of labeled data and to make NLP classification easier and less time-consuming, the researchers suggest applying transfer learning to NLP problems. Thus, instead of training the model from scratch, you can use another model that has been trained to solve a similar problem as the basis, and then fine-tune the original model to solve your specific problem.
   * This fine-tuning should take into account several important considerations: a) Different layers should be fine-tuned to different extents as they capture different kinds of information. b) Adapting model’s parameters to task-specific features will be more efficient if the learning rate is firstly linearly increased and then linearly decayed. c) Fine-tuning all layers at once is likely to result in catastrophic forgetting; thus, it would be better to gradually unfreeze the model starting from the last layer.
   * ULMFiT consists of three stages: a) The LM is trained on a general-domain corpus to capture general features of the language in different layers. b) The full LM is fine-tuned on target task data using discriminative fine-tuning and slanted triangular learning rates to learn task-specific features. c) The classifier is fine-tuned on the target task using gradual unfreezing and STLR to preserve low-level representations and adapt high-level ones.
2. Matthew E. Peters, Mark Neumann, Mohit Iyyer, Matt Gardner, Christopher Clark, Kenton Lee, Luke Zettlemoyer. [Deep contextualized word representations](https://arxiv.org/abs/1802.05365). arXiv:1802.05365, NAACL 2018. The source code is [ELMo](https://allennlp.org/elmo).
   * To generate word embeddings as a weighted sum of the internal states of a deep bi-directional language model (biLM), pre-trained on a large text corpus.
   * To include representations from all layers of a biLM as different layers represent different types of information.
   * To base ELMo representations on characters so that the network can use morphological clues to “understand” out-of-vocabulary tokens unseen in training.
3. Matthew E. Peters, Mark Neumann, Luke Zettlemoyer, Wen-tau Yih. [Dissecting Contextual Word Embeddings: Architecture and Representation](https://arxiv.org/abs/1808.08949v2). arXiv:1808.08949v2, EMNLP 2018.
3. Alec Radford, Karthik Narasimhan, Tim Salimans, and Ilya Sutskever. [Improving Language Understanding by Generative Pre-Training](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf). Technical report, OpenAI, 2018. The source code written in Python is [finetune-transformer-lm](https://github.com/openai/finetune-transformer-lm).
4. Jacob Devlin, Ming-Wei Chang, Kenton Lee, Kristina Toutanova. [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805). arXiv:1810.04805, 2018.
   * TensorFlow code and pre-trained models for BERT are in [bert](https://github.com/google-research/bert).
   *  PyTorch versions of BERT are [pytorch-pretrained-BERT](https://github.com/huggingface/pytorch-pretrained-BERT) and [BERT-pytorch](https://github.com/codertimo/BERT-pytorch).
   *  Chainer implementation of BERT is [bert-chainer](https://github.com/soskek/bert-chainer).
   *  Using BERT model as a sentence encoding service is implemented as [bert-as-service](https://github.com/hanxiao/bert-as-service).
5. Xiaodong Liu, Pengcheng He, Weizhu Chen, Jianfeng Gao. [Multi-Task Deep Neural Networks for Natural Language Understanding](https://arxiv.org/abs/1901.11504). arXiv:1901.11504, 2019. The PyTorch package implements this paper, named as [mt-dnn](https://github.com/namisan/mt-dnn).


#### Cross-lingual Language Representations

1. Guillaume Lample, Alexis Conneau. [Cross-lingual Language Model Pretraining](https://arxiv.org/abs/1901.07291). arXiv:1901.07291, 2019.


### Extractive Text Summarization

1. H. P. Luhn. [The automatic creation of literature abstracts](http://courses.ischool.berkeley.edu/i256/f06/papers/luhn58.pdf). IBM Journal of Research and Development, 1958. Luhn's method is as follows:
   1. Ignore Stopwords: Common words (known as stopwords) are ignored.
   2. Determine Top Words: The most often occuring words in the document are counted up.
   3. Select Top Words: A small number of the top words are selected to be used for scoring.
   4. Select Top Sentences: Sentences are scored according to how many of the top words they contain. The top four sentences are selected for the summary.
2. H. P. Edmundson. [New Methods in Automatic Extracting](http://courses.ischool.berkeley.edu/i256/f06/papers/edmonson69.pdf). Journal of the Association for Computing Machinery, 1969.
3. David M. Blei, Andrew Y. Ng and Michael I. Jordan. [Latent Dirichlet Allocation](http://ai.stanford.edu/~ang/papers/jair03-lda.pdf). Journal of Machine Learning Research, 2003. The source code in Python is [sklearn.decomposition.LatentDirichletAllocation](http://scikit-learn.org/dev/auto_examples/applications/plot_topics_extraction_with_nmf_lda.html). Reimplement Luhn's algorithm, but with topics instead of words and applied to several documents instead of one.
   1. Train LDA on all products of a certain type (e.g. all the books)
   2. Treat all the reviews of a particular product as one document, and infer their topic distribution
   3. Infer the topic distribution for each sentence
   4. For each topic that dominates the reviews of a product, pick some sentences that are themselves dominated by that topic.
4. David M. Blei. [Probabilistic Topic Models](http://www.cs.columbia.edu/~blei/papers/Blei2012.pdf). Communications of the ACM, 2012.
5. Rada Mihalcea and Paul Tarau. [TextRank: Bringing Order into Texts](https://web.eecs.umich.edu/~mihalcea/papers/mihalcea.emnlp04.pdf). ACL, 2004. The source code in Python is [pytextrank](https://github.com/ceteri/pytextrank). `pytextrank` works in four stages, each feeding its output to the next:
   - Part-of-Speech Tagging and lemmatization are performed for every sentence in the document.
   - Key phrases are extracted along with their counts, and are normalized.
   - Calculates a score for each sentence by approximating jaccard distance between the sentence and key phrases.
   - Summarizes the document based on most significant sentences and key phrases.
6. Federico Barrios, Federico López, Luis Argerich and Rosa Wachenchauzer. [Variations of the Similarity Function of TextRank for Automated Summarization](https://arxiv.org/abs/1602.03606). arXiv:1602.03606, 2016. The source code in Python is [gensim.summarization](http://radimrehurek.com/gensim/). Gensim's summarization only works for English for now, because the text is pre-processed so that stop words are removed and the words are stemmed, and these processes are language-dependent. TextRank works as follows:
   - Pre-process the text: remove stop words and stem the remaining words.
   - Create a graph where vertices are sentences.
   - Connect every sentence to every other sentence by an edge. The weight of the edge is how similar the two sentences are.
   - Run the PageRank algorithm on the graph.
   - Pick the vertices(sentences) with the highest PageRank score.
7. [TextTeaser](https://github.com/MojoJolo/textteaser) uses basic summarization features and build from it. Those features are:
   - Title feature is used to score the sentence with the regards to the title. It is calculated as the count of words which are common to title of the document and sentence.
   - Sentence length is scored depends on how many words are in the sentence. TextTeaser defined a constant “ideal” (with value 20), which represents the ideal length of the summary, in terms of number of words. Sentence length is calculated as a normalized distance from this value.
   - Sentence position is where the sentence is located. I learned that introduction and conclusion will have higher score for this feature.
   - Keyword frequency is just the frequency of the words used in the whole text in the bag-of-words model (after removing stop words).
8. Güneş Erkan and Dragomir R. Radev. [LexRank: Graph-based Lexical Centrality as Salience in Text Summarization](https://www.cs.cmu.edu/afs/cs/project/jair/pub/volume22/erkan04a-html/erkan04a.html). 2004.
   - LexRank uses IDF-modified Cosine as the similarity measure between two sentences. This similarity is used as weight of the graph edge between two sentences. LexRank also incorporates an intelligent post-processing step which makes sure that top sentences chosen for the summary are not too similar to each other.
9. [Latent Semantic Analysis(LSA) Tutorial](https://technowiki.wordpress.com/2011/08/27/latent-semantic-analysis-lsa-tutorial/).
10. Josef Steinberger and Karel Jezek. [Using Latent Semantic Analysis in Text Summarization and Summary Evaluation](http://www.kiv.zcu.cz/~jstein/publikace/isim2004.pdf). Proc. ISIM’04, 2004.
11. Josef Steinberger and Karel Ježek. [Text summarization and singular value decomposition](https://www.researchgate.net/profile/Karel_Jezek2/publication/226424326_Text_Summarization_and_Singular_Value_Decomposition/links/57233c1308ae586b21d87e66/Text-Summarization-and-Singular-Value-Decomposition.pdf). International Conference on Advances in Information Systems, 2004.
12. Josef Steinberger, Massimo Poesio, Mijail A Kabadjov and Karel Ježek. [Two uses of anaphora resolution in summarization](http://www.sensei-conversation.eu/wp-content/uploads/files/IPMpaper_official.pdf). Information Processing & Management, 2007.
13. James Clarke and Mirella Lapata. [Modelling Compression with Discourse Constraints](http://jamesclarke.net/media/papers/clarke-lapata-emnlp07.pdf). EMNLP-CoNLL, 2007.
14. Dan Gillick and Benoit Favre. [A Scalable Global Model for Summarization](https://pdfs.semanticscholar.org/a1a2/748e68d019815f1107fa19b0ab628b63928a.pdf). ACL, 2009.
15. Ani Nenkova and Kathleen McKeown. [Automatic summarization](https://www.cis.upenn.edu/~nenkova/1500000015-Nenkova.pdf).
Foundations and Trend in Information Retrieval, 2011. [The slides](https://www.fosteropenscience.eu/sites/default/files/pdf/2932.pdf) are also available.
16. Vahed Qazvinian, Dragomir R. Radev, Saif M. Mohammad, Bonnie Dorr, David Zajic, Michael Whidby, Taesun Moon. [Generating Extractive Summaries of Scientific Paradigms](https://arxiv.org/abs/1402.0556v1). arXiv:1402.0556, 2014.
17. Kågebäck, Mikael, et al. [Extractive summarization using continuous vector space models](http://www.aclweb.org/anthology/W14-1504). Proceedings of the 2nd Workshop on Continuous Vector Space Models and their Compositionality (CVSC)@ EACL. 2014.
18. Katja Filippova, Enrique Alfonseca, Carlos A. Colmenares, Lukasz Kaiser, Oriol Vinyals. [Sentence Compression by Deletion with LSTMs](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/43852.pdf). EMNLP 2015.
18. Ramesh Nallapati, Bowen Zhou, Mingbo Ma. [Classify or Select: Neural Architectures for Extractive Document Summarization](https://arxiv.org/abs/1611.04244).  arXiv:1611.04244. 2016.
19. Liangguo Wang, Jing Jiang, Hai Leong Chieu, Chen Hui Ong, Dandan Song, Lejian Liao. [Can Syntax Help? Improving an LSTM-based Sentence Compression Model for New Domains](http://www.aclweb.org/anthology/P17-1127). ACL 2017.
19. Ramesh Nallapati, Feifei Zhai, Bowen Zhou. [SummaRuNNer: A Recurrent Neural Network based Sequence Model for Extractive Summarization of Documents](https://arxiv.org/abs/1611.04230). arXiv:1611.04230, AAAI 2017.
20. Shashi Narayan, Nikos Papasarantopoulos, Mirella Lapata, Shay B. Cohen. [Neural Extractive Summarization with Side Information](https://arxiv.org/abs/1704.04530). arXiv:1704.04530, 2017.
21. Rakesh Verma, Daniel Lee. [Extractive Summarization: Limits, Compression, Generalized Model and Heuristics](https://arxiv.org/abs/1704.05550v1). arXiv:1704.05550, 2017.
22. Ed Collins, Isabelle Augenstein, Sebastian Riedel. [A Supervised Approach to Extractive Summarisation of Scientific Papers](https://arxiv.org/abs/1706.03946v1). arXiv:1706.03946, 2017.
23. Sukriti Verma, Vagisha Nidhi. [Extractive Summarization using Deep Learning](https://arxiv.org/abs/1708.04439v1). arXiv:1708.04439, 2017.
24. Parth Mehta, Gaurav Arora, Prasenjit Majumder. [Attention based Sentence Extraction from Scientific Articles using Pseudo-Labeled data](https://arxiv.org/abs/1802.04675v1).     arXiv:1802.04675, 2018.
25. Shashi Narayan, Shay B. Cohen, Mirella Lapata. [Ranking Sentences for Extractive Summarization with Reinforcement Learning](https://arxiv.org/abs/1802.08636v1). arXiv:1802.08636, NAACL, 2018.
26. Aakash Sinha, Abhishek Yadav, Akshay Gahlot. [Extractive Text Summarization using Neural Networks](https://arxiv.org/abs/1802.10137v1). arXiv:1802.10137, 2018.
27. Yuxiang Wu, Baotian Hu. [Learning to Extract Coherent Summary via Deep Reinforcement Learning](https://arxiv.org/abs/1804.07036). arXiv:1804.07036, AAAI, 2018.
28. Tanner A. Bohn, Charles X. Ling. [Neural Sentence Location Prediction for Summarization](https://arxiv.org/abs/1804.08053v1). arXiv:1804.08053, 2018.
28. Kamal Al-Sabahi, Zhang Zuping, Mohammed Nadher. [A Hierarchical Structured Self-Attentive Model for Extractive Document Summarization (HSSAS)](https://arxiv.org/abs/1805.07799v1). arXiv:1805.07799, IEEE Access, 2018.
28. Sansiri Tarnpradab, Fei Liu, Kien A. Hua. [Toward Extractive Summarization of Online Forum Discussions via Hierarchical Attention Networks](https://arxiv.org/abs/1805.10390v2). arXiv:1805.10390v2, 2018.
28. Kristjan Arumae, Fei Liu. [Reinforced Extractive Summarization with Question-Focused Rewards](https://arxiv.org/abs/1805.10392v2). arXiv:1805.10392, 2018.
28. Qingyu Zhou, Nan Yang, Furu Wei, Shaohan Huang, Ming Zhou, Tiejun Zhao. [Neural Document Summarization by Jointly Learning to Score and Select Sentences](https://arxiv.org/abs/1807.02305v1). arXiv:1807.02305, ACL 2018.
28. Xingxing Zhang, Mirella Lapata, Furu Wei, Ming Zhou. [Neural Latent Extractive Document Summarization](https://arxiv.org/abs/1808.07187v2). arXiv:1808.07187, EMNLP 2018.
29. Yue Dong, Yikang Shen, Eric Crawford, Herke van Hoof, Jackie Chi Kit Cheung. [BanditSum: Extractive Summarization as a Contextual Bandit](https://arxiv.org/abs/1809.09672v3). arXiv:1809.09672v3, EMNLP 2018.
29. Chandra Shekhar Yadav. [Automatic Text Document Summarization using Semantic-based Analysis](https://arxiv.org/abs/1811.06567v1). arXiv:1811.06567, 2018.
1. Aishwarya Jadhav, Vaibhav Rajan. [Extractive Summarization with SWAP-NET: Sentences and Words from Alternating Pointer Networks](https://www.aclweb.org/anthology/P18-1014/). ACL, 2018.
30. Jiacheng Xu, Greg Durrett. [Neural Extractive Text Summarization with Syntactic Compression](https://arxiv.org/abs/1902.00863). arXiv:1902.00863v1, 2019.
31. John Brandt. [Imbalanced multi-label classification using multi-task learning with extractive summarization](https://arxiv.org/abs/1903.06963v1). arXiv:1903.06963v1, 2019.
31. Yang Liu. [Fine-tune BERT for Extractive Summarization](https://arxiv.org/abs/1903.10318v2). arXiv:1903.10318v2 , 2019. The source code is  [BertSum](https://github.com/nlpyang/BertSum).
32. Kristjan Arumae, Fei Liu. [Guiding Extractive Summarization with Question-Answering Rewards](https://arxiv.org/abs/1904.02321v1). arXiv:1904.02321v1, NAACL 2019.
32. Xingxing Zhang, Furu Wei, Ming Zhou. [HIBERT: Document Level Pre-training of Hierarchical Bidirectional Transformers for Document Summarization](https://arxiv.org/abs/1905.06566v1). arXiv:1905.06566v1, ACL 2019.
32. Sangwoo Cho, Logan Lebanoff, Hassan Foroosh, Fei Liu. [Improving the Similarity Measure of Determinantal Point Processes for Extractive Multi-Document Summarization](https://arxiv.org/abs/1906.00072v1). arXiv:1906.00072v1, ACL 2019.
33. Derek Miller. [Leveraging BERT for Extractive Text Summarization on Lectures](https://arxiv.org/abs/1906.04165v1). arXiv:1906.04165v1, 2019.
34. Hong Wang, Xin Wang, Wenhan Xiong, Mo Yu, Xiaoxiao Guo, Shiyu Chang, William Yang Wang. [Self-Supervised Learning for Contextualized Extractive Summarization](https://arxiv.org/abs/1906.04466v1). arXiv:1906.04466v1, ACL 2019.
35. Kai Wang, Xiaojun Quan, Rui Wang. [BiSET: Bi-directional Selective Encoding with Template for Abstractive Summarization](https://arxiv.org/abs/1906.05012v1). arXiv:1906.05012v1, 2019.
36. Hadrien Van Lierde, Tommy W. S. Chow. [Learning with fuzzy hypergraphs: a topical approach to query-oriented text summarization](https://arxiv.org/abs/1906.09445v1). arXiv:1906.09445v1, 2019.
37. Ming Zhong, Pengfei Liu, Danqing Wang, Xipeng Qiu, Xuanjing Huang. [Searching for Effective Neural Extractive Summarization: What Works and What's Next](https://arxiv.org/abs/1907.03491v1). arXiv:1907.03491v1, ACL 2019.
32. Léo Bouscarrat, Antoine Bonnefoy, Thomas Peel, Cécile Pereira. [STRASS: A Light and Effective Method for Extractive Summarization Based on Sentence Embeddings](https://arxiv.org/abs/1907.07323v1). arXiv:1907.07323v1, 2019.
34. Danqing Wang, Pengfei Liu, Ming Zhong, Jie Fu, Xipeng Qiu, Xuanjing Huang. [Exploring Domain Shift in Extractive Text Summarization](https://arxiv.org/abs/1908.11664v1). arXiv:1908.11664v1, 2019.
1. Sandeep Subramanian, Raymond Li, Jonathan Pilault, Christopher Pal. [On Extractive and Abstractive Neural Document Summarization with Transformer Language Models](https://arxiv.org/abs/1909.03186v2). arXiv:1909.03186v2, 2019.
1. Sanghwan Bae, Taeuk Kim, Jihoon Kim, Sang-goo Lee. [Summary Level Training of Sentence Rewriting for Abstractive Summarization](https://arxiv.org/abs/1909.08752v3). arXiv:1909.08752v3, 2019.
1. Jiacheng Xu, Zhe Gan, Yu Cheng, Jingjing Liu. [Discourse-Aware Neural Extractive Model for Text Summarization](https://arxiv.org/abs/1910.14142v2).  arXiv:1910.14142v2, ACL 2020. The source code is [DiscoBERT](https://github.com/jiacheng-xu/DiscoBERT).
1. Eduardo Brito, Max Lübbering, David Biesner, Lars Patrick Hillebrand, Christian Bauckhage. [Towards Supervised Extractive Text Summarization via RNN-based Sequence Classification](https://arxiv.org/abs/1911.06121v1). arXiv:1911.06121v1, 2019.
1. Vivian T. Chou, LeAnna Kent, Joel A. Góngora, Sam Ballerini, Carl D. Hoover. [Towards automatic extractive text summarization of A-133 Single Audit reports with machine learning](https://arxiv.org/abs/1911.06197v1). rXiv:1911.06197v1, 2019.
1. Abhishek Kumar Singh, Manish Gupta, Vasudeva Varma. [Unity in Diversity: Learning Distributed Heterogeneous Sentence Representation for Extractive Summarization](https://arxiv.org/abs/1912.11688v1). arXiv:1912.11688v1, 2019.
1. Abhishek Kumar Singh, Manish Gupta, Vasudeva Varma. [Hybrid MemNet for Extractive Summarization](https://arxiv.org/abs/1912.11701v1). arXiv:1912.11701v1, 2019.
1. Ahmed Magooda, Cezary Marcjan. [Attend to the beginning: A study on using bidirectional attention for extractive summarization](https://arxiv.org/abs/2002.03405v3). arXiv:2002.03405v3, FLAIRS33 2020.
1. Qingyu Zhou, Furu Wei, Ming Zhou. [At Which Level Should We Extract? An Empirical Study on Extractive Document Summarization](https://arxiv.org/abs/2004.02664v1). arXiv:2004.02664v1, 2020.
1. Leon Schüller, Florian Wilhelm, Nico Kreiling, Goran Glavaš. [Windowing Models for Abstractive Summarization of Long Texts](https://arxiv.org/abs/2004.03324v1). arXiv:2004.03324v1, 2020.
1. Keping Bi, Rahul Jha, W. Bruce Croft, Asli Celikyilmaz. [AREDSUM: Adaptive Redundancy-Aware Iterative Sentence Ranking for Extractive Document Summarization](https://arxiv.org/abs/2004.06176v1). arXiv:2004.06176v1, 2020.
1. Ming Zhong, Pengfei Liu, Yiran Chen, Danqing Wang, Xipeng Qiu, Xuanjing Huang. [Extractive Summarization as Text Matching](https://arxiv.org/abs/2004.08795v1). arXiv:2004.08795v1, 2020. The official code is implemented as [MatchSum](https://github.com/maszhongming/MatchSum).
1. Danqing Wang, Pengfei Liu, Yining Zheng, Xipeng Qiu, Xuanjing Huang. [Heterogeneous Graph Neural Networks for Extractive Document Summarization](https://arxiv.org/abs/2004.12393v1). arXiv:2004.12393v1, ACL 2020.
1. Zhengyuan Liu, Ke Shi, Nancy F. Chen. [Conditional Neural Generation using Sub-Aspect Functions for Extractive News Summarization](https://arxiv.org/abs/2004.13983v2). arXiv:2004.13983v2, 2020.
1. Yue Dong, Andrei Romascanu, Jackie C. K. Cheung. [HipoRank: Incorporating Hierarchical and Positional Information into Graph-based Unsupervised Long Document Extractive Summarization](https://arxiv.org/abs/2005.00513v1). arXiv:2005.00513v1, 2020.
1. Jong Won Park. [Continual BERT: Continual Learning for Adaptive Extractive Summarization of COVID-19 Literature](https://arxiv.org/abs/2007.03405v1). arXiv:2007.03405v1, 2020.
1. Daniel Lee, Rakesh Verma, Avisha Das, Arjun Mukherjee. [Experiments in Extractive Summarization: Integer Linear Programming, Term/Sentence Scoring, and Title-driven Models](https://arxiv.org/abs/2008.00140v1). arXiv:2008.00140v1, 2020.


### Abstractive Text Summarization

1. Alexander M. Rush, Sumit Chopra, Jason Weston. [A Neural Attention Model for Abstractive Sentence Summarization](https://arxiv.org/abs/1509.00685). EMNLP, 2015. The source code in LUA Torch7 is [NAMAS](https://github.com/facebook/NAMAS).
   - They use sequence-to-sequence encoder-decoder LSTM with attention.
   - They use the first sentence of a document. The source document is quite small (about 1 paragraph or ~500 words in the training dataset of Gigaword) and the produced output is also very short (about 75 characters). It remains an open challenge to scale up these limits - to produce longer summaries over multi-paragraph text input (even good LSTM models with attention models fall victim to vanishing gradients when the input sequences become longer than a few hundred items).
   - The evaluation method used for automatic summarization has traditionally been the ROUGE metric - which has been shown to correlate well with human judgment of summary quality, but also has a known tendency to encourage "extractive" summarization - so that using ROUGE as a target metric to optimize will lead a summarizer towards a copy-paste behavior of the input instead of the hoped-for reformulation type of summaries.
2. Peter Liu and Xin Pan. [Sequence-to-Sequence with Attention Model for Text Summarization](https://research.googleblog.com/2016/08/text-summarization-with-tensorflow.html). 2016. The source code in Python is [textsum](https://github.com/tensorflow/models/tree/master/textsum).
   - They use sequence-to-sequence encoder-decoder LSTM with attention and bidirectional neural net.
   - They use the first 2 sentences of a document with a limit at 120 words.
   - The scores achieved by Google’s *textsum* are 42.57 ROUGE-1 and 23.13 ROUGE-2.
3. Ramesh Nallapati, Bowen Zhou, Cicero Nogueira dos santos, Caglar Gulcehre, Bing Xiang. [Abstractive Text Summarization Using Sequence-to-Sequence RNNs and Beyond](https://arxiv.org/abs/1602.06023). arXiv:1602.06023, 2016. The souce code written in Python is [Summarization](https://github.com/zwc12/Summarization) or [abstractive-text-summarization](https://github.com/alesee/abstractive-text-summarization).
   - They use GRU with attention and bidirectional neural net.
   - They use the first 2 sentences of a documnet with a limit at 120 words.
   - They use the [Large vocabulary trick (LVT)](https://arxiv.org/abs/1412.2007) of Jean et al. 2014, which means when you decode, use only the words that appear in the source - this reduces perplexity. But then you lose the capability to do "abstractive" summary. So they do "vocabulary expansion" by adding a layer of "word2vec nearest neighbors" to the words in the input.
   - Feature rich encoding - they add TFIDF and Named Entity types to the word embeddings (concatenated) to the encodings of the words - this adds to the encoding dimensions that reflect "importance" of the words. 
   - The most interesting of all is what they call the "Switching Generator/Pointer" layer. In the decoder, they add a layer that decides to either generate a new word based on the context / previously generated word (usual decoder) or copy a word from the input (that is - add a pointer to the input). They learn when to do Generate vs. Pointer and when it is a Pointer which word of the input to Point to.
4. Konstantin Lopyrev. [Generating News Headlines with Recurrent Neural Networks](https://arxiv.org/abs/1512.01712). arXiv:1512.01712, 2015. The source code in Python is [headlines](https://github.com/udibr/headlines).
5. Jiwei Li, Minh-Thang Luong and Dan Jurafsky. [A Hierarchical Neural Autoencoder for Paragraphs and Documents](https://arxiv.org/abs/1506.01057). arXiv:1506.01057, 2015. The source code in Matlab is [Hierarchical-Neural-Autoencoder](https://github.com/jiweil/Hierarchical-Neural-Autoencoder).
6. Sumit Chopra, Alexander M. Rush and Michael Auli. [Abstractive Sentence Summarization with Attentive Recurrent Neural Networks](http://harvardnlp.github.io/papers/naacl16_summary.pdf). NAACL, 2016.
7. Jianpeng Cheng, Mirella Lapata. [Neural Summarization by Extracting Sentences and Words](https://arxiv.org/abs/1603.07252). arXiv:1603.07252, 2016.
   - This paper uses attention as a mechanism for identifying the best sentences to extract, and then go beyond that to generate an abstractive summary.
8. Siddhartha Banerjee, Prasenjit Mitra, Kazunari Sugiyama. [Generating Abstractive Summaries from Meeting Transcripts](https://arxiv.org/abs/1609.07033v1). arXiv:1609.07033, Proceedings of the 2015 ACM Symposium on Document Engineering, DocEng' 2015.
9. Siddhartha Banerjee, Prasenjit Mitra, Kazunari Sugiyama. [Multi-document abstractive summarization using ILP based multi-sentence compression](https://arxiv.org/abs/1609.07034v1). arXiv:1609.07034, 2016.
10. Suzuki, Jun, and Masaaki Nagata. [Cutting-off Redundant Repeating Generations for Neural Abstractive Summarization](http://www.aclweb.org/anthology/E17-2047).  EACL 2017 (2017): 291.
11. Jiwei Tan and Xiaojun Wan. [Abstractive Document Summarization with a Graph-Based Attentional Neural Model](). ACL, 2017.
12. Preksha Nema, Mitesh M. Khapra, Balaraman Ravindran and Anirban Laha. [Diversity driven attention model for query-based abstractive summarization](). ACL,2017
13. Romain Paulus, Caiming Xiong, Richard Socher. [A Deep Reinforced Model for Abstractive Summarization](https://arxiv.org/abs/1705.04304). arXiv:1705.04304, 2017. The related blog is [Your tldr by an ai: a deep reinforced model for abstractive summarization](https://einstein.ai/research/your-tldr-by-an-ai-a-deep-reinforced-model-for-abstractive-summarization). 
    * Their model is trained with teacher forcing and reinforcement learning at the same time, being able to make use of both word-level and whole-summary-level supervision to make it more coherent and readable.
14. Shibhansh Dohare, Harish Karnick. [Text Summarization using Abstract Meaning Representation](https://arxiv.org/abs/1706.01678). arXiv:1706.01678, 2017.
15. Piji Li, Wai Lam, Lidong Bing, Zihao Wang. [Deep Recurrent Generative Decoder for Abstractive Text Summarization](https://arxiv.org/abs/1708.00625v1). arXiv:1708.00625, 2017.
16. Xinyu Hua, Lu Wang. [A Pilot Study of Domain Adaptation Effect for Neural Abstractive Summarization](https://arxiv.org/abs/1707.07062v1). arXiv:1707.07062, 2017.
1. Ziqiang Cao, Furu Wei, Wenjie Li, Sujian Li. [Faithful to the Original: Fact Aware Neural Abstractive Summarization](https://arxiv.org/abs/1711.04434v1). arXiv:1711.04434v1, 2017. 
17. Angela Fan, David Grangier, Michael Auli. [Controllable Abstractive Summarization](https://arxiv.org/abs/1711.05217v1). arXiv:1711.05217, 2017.
18. Linqing Liu, Yao Lu, Min Yang, Qiang Qu, Jia Zhu, Hongyan Li. [Generative Adversarial Network for Abstractive Text Summarization](https://arxiv.org/abs/1711.09357v1). arXiv:1711.09357, 2017.
19. Johan Hasselqvist, Niklas Helmertz, Mikael Kågebäck. [Query-Based Abstractive Summarization Using Neural Networks](https://arxiv.org/abs/1712.06100v1). arXiv:1712.06100, 2017.
20. Tal Baumel, Matan Eyal, Michael Elhadad. [Query Focused Abstractive Summarization: Incorporating Query Relevance, Multi-Document Coverage, and Summary Length Constraints into seq2seq Models](https://arxiv.org/abs/1801.07704v2). arXiv:1801.07704, 2018.
21. André Cibils, Claudiu Musat, Andreea Hossman, Michael Baeriswyl. [Diverse Beam Search for Increased Novelty in Abstractive Summarization](https://arxiv.org/abs/1802.01457v1). arXiv:1802.01457, 2018.
22. Chieh-Teng Chang, Chi-Chia Huang, Jane Yung-Jen Hsu. [A Hybrid Word-Character Model for Abstractive Summarization](https://arxiv.org/abs/1802.09968v1). arXiv:1802.09968, 2018.
23. Asli Celikyilmaz, Antoine Bosselut, Xiaodong He, Yejin Choi. [Deep Communicating Agents for Abstractive Summarization](https://arxiv.org/abs/1803.10357v1). arXiv:1803.10357, 2018.
24. Piji Li, Lidong Bing, Wai Lam. [Actor-Critic based Training Framework for Abstractive Summarization](https://arxiv.org/abs/1803.11070v1). arXiv:1803.11070, 2018.
25. Paul Azunre, Craig Corcoran, David Sullivan, Garrett Honke, Rebecca Ruppel, Sandeep Verma, Jonathon Morgan. [Abstractive Tabular Dataset Summarization via Knowledge Base Semantic Embeddings](https://arxiv.org/abs/1804.01503v2). arXiv:1804.01503, 2018.
26. Arman Cohan, Franck Dernoncourt, Doo Soon Kim, Trung Bui, Seokhwan Kim, Walter Chang, Nazli Goharian. [A Discourse-Aware Attention Model for Abstractive Summarization of Long Documents](https://arxiv.org/abs/1804.05685v1). arXiv:1804.05685, 2018.
27. Ramakanth Pasunuru, Mohit Bansal. [Multi-Reward Reinforced Summarization with Saliency and Entailment](https://arxiv.org/abs/1804.06451v1). arXiv:1804.06451, 2018.
28. Jianmin Zhang, Jiwei Tan, Xiaojun Wan. [Towards a Neural Network Approach to Abstractive Multi-Document Summarization](https://arxiv.org/abs/1804.09010v1). arXiv:1804.09010, 2018.
28. Shuming Ma, Xu Sun, Junyang Lin, Xuancheng Ren. [A Hierarchical End-to-End Model for Jointly Improving Text Summarization and Sentiment Classification](https://arxiv.org/abs/1805.01089v2). arXiv:1805.01089v2, IJCAI 2018.
28. Li Wang, Junlin Yao, Yunzhe Tao, Li Zhong, Wei Liu, Qiang Du. [A Reinforced Topic-Aware Convolutional Sequence-to-Sequence Model for Abstractive Text Summarization](https://arxiv.org/abs/1805.03616). arXiv:1805.03616, International Joint Conference on Artificial Intelligence and European Conference on Artificial Intelligence (IJCAI-ECAI), 2018.
29. Guokan Shang, Wensi Ding, Zekun Zhang, Antoine J.-P. Tixier, Polykarpos Meladianos, Michalis Vazirgiannis, Jean-Pierre Lorre´. [Unsupervised Abstractive Meeting Summarization with Multi-Sentence Compression and Budgeted Submodular Maximization](https://arxiv.org/abs/1805.05271). arXiv:1805.05271, 2018.
30. Fei Liu, Jeffrey Flanigan, Sam Thomson, Norman Sadeh, Noah A. Smith. [Toward Abstractive Summarization Using Semantic Representations](https://arxiv.org/abs/1805.10399v1). arXiv:1805.10399, 2018.
30. Han Guo, Ramakanth Pasunuru, Mohit Bansal. [Soft Layer-Specific Multi-Task Summarization with Entailment and Question Generation](https://arxiv.org/abs/1805.11004v1). arXiv:1805.11004, ACL 2018.
29. Yen-Chun Chen, Mohit Bansal. [Fast Abstractive Summarization with Reinforce-Selected Sentence Rewriting](https://arxiv.org/abs/1805.11080). arXiv:1805.11080, ACL 2018. The souce code written in Python is [fast_abs_rl](https://github.com/chenrocks/fast_abs_rl).
30. Reinald Kim Amplayo, Seonjae Lim, Seung-won Hwang. [Entity Commonsense Representation for Neural Abstractive Summarization](https://arxiv.org/abs/1806.05504v1). arXiv:1806.05504, NAACL 2018.
30. Kaiqiang Song, Lin Zhao, Fei Liu. [Structure-Infused Copy Mechanisms for Abstractive Summarization](https://arxiv.org/abs/1806.05658v2). arXiv:1806.05658v2, 2018. The source code is [struct_infused_summ](https://github.com/KaiQiangSong/struct_infused_summ).
31. Kexin Liao, Logan Lebanoff, Fei Liu. [Abstract Meaning Representation for Multi-Document Summarization](https://arxiv.org/abs/1806.05655v1). arXiv:1806.05655, 2018.
1. Chenliang Li, Weiran Xu, Si Li, Sheng Gao. [Guiding Generation for Abstractive Text Summarization Based on Key Information Guide Network](https://www.aclweb.org/anthology/N18-2009/). NAACL, June 2018.
30. Shibhansh Dohare, Vivek Gupta and Harish Karnick. [Unsupervised Semantic Abstractive Summarization](http://aclweb.org/anthology/P18-3011). ACL, July 2018.
1. Haoran Li, Junnan Zhu, Jiajun Zhang, Chengqing Zong. [Ensure the Correctness of the Summary: Incorporate Entailment Knowledge into Abstractive Sentence Summarization](https://www.aclweb.org/anthology/C18-1121/). COLING, August 2018.
31. Niantao Xie, Sujian Li, Huiling Ren, Qibin Zhai. [Abstractive Summarization Improved by WordNet-based Extractive Sentences](https://arxiv.org/abs/1808.01426v1). arXiv:1808.01426, NLPCC 2018.
31. Wojciech Kryściński, Romain Paulus, Caiming Xiong, Richard Socher. [Improving Abstraction in Text Summarization](https://arxiv.org/abs/1808.07913v1). arXiv:1808.07913, 2018.
1. Shashi Narayan, Shay B. Cohen, Mirella Lapata. [Don't Give Me the Details, Just the Summary! Topic-Aware Convolutional Neural Networks for Extreme Summarization](https://arxiv.org/abs/1808.08745v1). arXiv:1808.08745v1, 2018. The source code is [XSum](https://github.com/EdinburghNLP/XSum).
31. Hardy, Andreas Vlachos. [Guided Neural Language Generation for Abstractive Summarization using Abstract Meaning Representation](https://arxiv.org/abs/1808.09160v1). arXiv:1808.09160, EMNLP 2018.
31. Sebastian Gehrmann, Yuntian Deng, Alexander M. Rush. [Bottom-Up Abstractive Summarization](https://arxiv.org/abs/1808.10792v2). arXiv:1808.10792v2, 2018. The source code is [bottom-up-summary](https://github.com/sebastianGehrmann/bottom-up-summary)
31. Yichen Jiang, Mohit Bansal. [Closed-Book Training to Improve Summarization Encoder Memory](https://arxiv.org/abs/1809.04585v1). arXiv:1809.04585, 2018.
30. Raphael Schumann. [Unsupervised Abstractive Sentence Summarization using Length Controlled Variational Autoencoder](https://arxiv.org/abs/1809.05233). arXiv:1809.05233, 2018.
31. Kamal Al-Sabahi, Zhang Zuping, Yang Kang. [Bidirectional Attentional Encoder-Decoder Model and Bidirectional Beam Search for Abstractive Summarization](https://arxiv.org/abs/1809.06662v1). arXiv:1809.06662, 2018.
32. Tomonori Kodaira, Mamoru Komachi. [The Rule of Three: Abstractive Text Summarization in Three Bullet Points](https://arxiv.org/abs/1809.10867v1). arXiv:1809.10867, PACLIC 2018, 2018.
32. Byeongchang Kim, Hyunwoo Kim, Gunhee Kim. [Abstractive Summarization of Reddit Posts with Multi-level Memory Networks](https://arxiv.org/abs/1811.00783). arXiv:1811.00783, 2018. The github project is  [MMN](https://github.com/ctr4si/MMN) including the dataset.
33. Tian Shi, Yaser Keneshloo, Naren Ramakrishnan, Chandan K. Reddy. [Neural Abstractive Text Summarization with Sequence-to-Sequence Models: A Survey](https://arxiv.org/abs/1812.02303v3). arXiv:1812.02303v3, 2018.
1. Wei Li, Xinyan Xiao, Yajuan Lyu, Yuanzhuo Wang. [Improving Neural Abstractive Document Summarization with Explicit Information Selection Modeling](https://www.aclweb.org/anthology/D18-1205/). EMNLP, 2018.
1. Wei Li, Xinyan Xiao, Yajuan Lyu, Yuanzhuo Wang. [Improving Neural Abstractive Document Summarization with Structural Regularization](https://www.aclweb.org/anthology/D18-1441/). EMNLP, 2018.
34. Shen Gao, Xiuying Chen, Piji Li, Zhaochun Ren, Lidong Bing, Dongyan Zhao, Rui Yan. [Abstractive Text Summarization by Incorporating Reader Comments](https://arxiv.org/abs/1812.05407v1).  arXiv:1812.05407v1, AAAI 2019.
35. Haoyu Zhang, Yeyun Gong, Yu Yan, Nan Duan, Jianjun Xu, Ji Wang, Ming Gong, Ming Zhou. [Pretraining-Based Natural Language Generation for Text Summarization](https://arxiv.org/abs/1902.09243v2). arXiv:1902.09243v2, 2019.
1. Yong Zhang, Dan Li, Yuheng Wang, Yang Fang, and Weidong Xiao. [Abstract Text Summarization with a Convolutional Seq2seq Model](https://www.mdpi.com/2076-3417/9/8/1665/pdf). MDPI Applied Sciences, 2019.
36. Soheil Esmaeilzadeh, Gao Xian Peh, Angela Xu. [Neural Abstractive Text Summarization and Fake News Detection](https://arxiv.org/abs/1904.00788). arXiv:1904.00788v1, 2019.
1. Li Dong, Nan Yang, Wenhui Wang, Furu Wei, Xiaodong Liu, Yu Wang, Jianfeng Gao, Ming Zhou, Hsiao-Wuen Hon. [Unified Language Model Pre-training for Natural Language Understanding and Generation](https://arxiv.org/abs/1905.03197v3). arXiv:1905.03197v3, 2019. The source code is [unilm](https://github.com/microsoft/unilm).
37. Sean MacAvaney, Sajad Sotudeh, Arman Cohan, Nazli Goharian, Ish Talati, Ross W. Filice. [Ontology-Aware Clinical Abstractive Summarization](https://arxiv.org/abs/1905.05818v1). arXiv:1905.05818v1, SIGIR 2019 Short Paper.
38. Urvashi Khandelwal, Kevin Clark, Dan Jurafsky, Lukasz Kaiser. [Sample Efficient Text Summarization Using a Single Pre-Trained Transformer](https://arxiv.org/abs/1905.08836v1). arXiv:1905.08836v1, 2019.
37. Logan Lebanoff, Kaiqiang Song, Franck Dernoncourt, Doo Soon Kim, Seokhwan Kim, Walter Chang, Fei Liu. [Scoring Sentence Singletons and Pairs for Abstractive Summarization](https://arxiv.org/abs/1906.00077v1). arXiv:1906.00077v1, ACL 2019.
38. Andrew Hoang, Antoine Bosselut, Asli Celikyilmaz, Yejin Choi. [Efficient Adaptation of Pretrained Transformers for Abstractive Summarization](https://arxiv.org/abs/1906.00138v1). arXiv:1906.00138v1, 2019.
39. Matan Eyal, Tal Baumel, Michael Elhadad. [Question Answering as an Automatic Evaluation Metric for News Article Summarization](https://arxiv.org/abs/1906.00318v1). arXiv:1906.00318v1, NAACL 2019.
40. Laura Manor, Junyi Jessy Li. [Plain English Summarization of Contracts](https://arxiv.org/abs/1906.00424v1).  arXiv:1906.00424v1, 2019.
41. Alexander R. Fabbri, Irene Li, Tianwei She, Suyi Li, Dragomir R. Radev. [Multi-News: a Large-Scale Multi-Document Summarization Dataset and Abstractive Hierarchical Model](https://arxiv.org/abs/1906.01749v3). arXiv:1906.01749v3, ACL 2019.
41. Eva Sharma, Chen Li, Lu Wang. [BIGPATENT: A Large-Scale Dataset for Abstractive and Coherent Summarization](https://arxiv.org/abs/1906.03741v1). arXiv:1906.03741v1, ACL 2019.
42. Masaru Isonuma, Junichiro Mori, Ichiro Sakata. [Unsupervised Neural Single-Document Summarization of Reviews via Learning Latent Discourse Structure and its Ranking](https://arxiv.org/abs/1906.05691v1). arXiv:1906.05691v1, ACL 2019.
43. Joris Baan, Maartje ter Hoeve, Marlies van der Wees, Anne Schuth, Maarten de Rijke. [Do Transformer Attention Heads Provide Transparency in Abstractive Summarization?](https://arxiv.org/abs/1907.00570v2). arXiv:1907.00570v2, FACTS-IR 2019, SIGIR.
43. Saadia Gabriel, Antoine Bosselut, Ari Holtzman, Kyle Lo, Asli Celikyilmaz, Yejin Choi. [Cooperative Generator-Discriminator Networks for Abstractive Summarization with Narrative Flow](https://arxiv.org/abs/1907.01272v1). arXiv:1907.01272v1, 2019.
37. Shashi Narayan, Shay B. Cohen, Mirella Lapata. [What is this Article about? Extreme Summarization with Topic-aware Convolutional Neural Networks](https://arxiv.org/abs/1907.08722v1). arXiv:1907.08722v1, 2019.
38. Nikola I. Nikolov, Richard H.R. Hahnloser. [Abstractive Document Summarization without Parallel Data](https://arxiv.org/abs/1907.12951v2).  arXiv:1907.12951v2, LREC 2020.
39. Melissa Ailem, Bowen Zhang, Fei Sha. [Topic Augmented Generator for Abstractive Summarization](https://arxiv.org/abs/1908.07026v1). arXiv:1908.07026v1, 2019.
40. Siyao Li, Deren Lei, Pengda Qin, William Yang Wang. [Deep Reinforcement Learning with Distributional Semantic Rewards for Abstractive Summarization](https://arxiv.org/abs/1909.00141v1). arXiv:1909.00141v1, 2019.
37. Luke de Oliveira, Alfredo Láinez Rodrigo. [Repurposing Decoder-Transformer Language Models for Abstractive Summarization](https://arxiv.org/abs/1909.00325v1). arXiv:1909.00325v1, 2019.
1. Eric Malmi, Sebastian Krause, Sascha Rothe, Daniil Mirylenka, Aliaksei Severyn. [Encode, Tag, Realize: High-Precision Text Editing](https://arxiv.org/abs/1909.01187v1). arXiv:1909.01187v1, EMNLP 2019. The source code is [lasertagger](https://github.com/google-research/lasertagger).
1. Jaemin Cho, Minjoon Seo, Hannaneh Hajishirzi. [Mixture Content Selection for Diverse Sequence Generation](https://arxiv.org/abs/1909.01953v1). arXiv:1909.01953v1, EMNLP-IJCNLP 2019. The source code is [FocusSeq2Seq](https://github.com/clovaai/FocusSeq2Seq).
37. Eva Sharma, Luyang Huang, Zhe Hu, Lu Wang. [An Entity-Driven Framework for Abstractive Summarization](https://arxiv.org/abs/1909.02059v1). arXiv:1909.02059v1, 2019.
1. Sanghwan Bae, Taeuk Kim, Jihoon Kim, Sang-goo Lee. [Summary Level Training of Sentence Rewriting for Abstractive Summarization](https://arxiv.org/abs/1909.08752v3). arXiv:1909.08752v3, 2019.
1. Lei Li, Wei Liu, Marina Litvak, Natalia Vanetik, Zuying Huang. [In Conclusion Not Repetition: Comprehensive Abstractive Summarization With Diversified Attention Based On Determinantal Point Processes](https://arxiv.org/abs/1909.10852v2). arXiv:1909.10852v2, 2019.
1. Peter J. Liu, Yu-An Chung, Jie Ren. [SummAE: Zero-Shot Abstractive Text Summarization using Length-Agnostic Auto-Encoders](https://arxiv.org/abs/1910.00998v1). arXiv:1910.00998v1, 2019.
1. Wang Wenbo, Gao Yang, Huang Heyan, Zhou Yuxiang. [Concept Pointer Network for Abstractive Summarization](https://arxiv.org/abs/1910.08486). arXiv:1910.08486v1, 2019.
1. Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, Peter J. Liu. [Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer](https://arxiv.org/abs/1910.10683v3). arXiv:1910.10683v3, 2019. The source code is [text-to-text-transfer-transformer](https://github.com/google-research/text-to-text-transfer-transformer).
1. Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Ves Stoyanov, Luke Zettlemoyer. [BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension](https://arxiv.org/abs/1910.13461v1). arXiv:1910.13461v1, 2019. The source code is [bart](https://github.com/pytorch/fairseq/tree/master/examples/bart).
1. Kaiqiang Song, Logan Lebanoff, Qipeng Guo, Xipeng Qiu, Xiangyang Xue, Chen Li, Dong Yu, Fei Liu. [Joint Parsing and Generation for Abstractive Summarization](https://arxiv.org/abs/1911.10389v1). arXiv:1911.10389v1, 2019. The source code is [joint_parse_summ](https://github.com/KaiQiangSong/joint_parse_summ).
1. Kaiqiang Song, Bingqing Wang, Zhe Feng, Liu Ren, Fei Liu. [Controlling the Amount of Verbatim Copying in Abstractive Summarization](https://arxiv.org/abs/1911.10390v1). arXiv:1911.10390v1, 2019.
1. Sebastian Gehrmann, Zachary Ziegler, Alexander Rush. [Generating Abstractive Summaries with Finetuned Language Models](https://www.aclweb.org/anthology/W19-8665/). SIGGEN, October–November 2019.
1. Hyungtak Choi, Lohith Ravuru, Tomasz Dryjański, Sunghan Rye, Donghyun Lee, Hojung Lee, Inchul Hwang. [VAE-PGN based Abstractive Model in Multi-stage Architecture for Text Summarization](https://www.aclweb.org/anthology/W19-8664/). SIGGEN, October–November 2019.
1. Jingqing Zhang, Yao Zhao, Mohammad Saleh, Peter J. Liu. [PEGASUS: Pre-training with Extracted Gap-sentences for Abstractive Summarization](https://arxiv.org/abs/1912.08777v3). arXiv:1912.08777v3, 2019.
1. Pengcheng Liao, Chuang Zhang, Xiaojun Chen, Xiaofei Zhou. [Improving Abstractive Text Summarization with History Aggregation](https://arxiv.org/abs/1912.11046v1). arXiv:1912.11046v1, 2019.
1. Ankit Chadha, Mohamed Masoud. [Deep Reinforced Self-Attention Masks for Abstractive Summarization (DR.SAS)](https://arxiv.org/abs/2001.00009v1). arXiv:2001.00009v1, 2020.
1. Ziyi Yang, Chenguang Zhu, Robert Gmyr, Michael Zeng, Xuedong Huang, Eric Darve. [TED: A Pretrained Unsupervised Summarization Model with Theme Modeling and Denoising](https://arxiv.org/abs/2001.00725v2). arXiv:2001.00725v2, 2020.
1. Yu Yan, Weizhen Qi, Yeyun Gong, Dayiheng Liu, Nan Duan, Jiusheng Chen, Ruofei Zhang, Ming Zhou. [ProphetNet: Predicting Future N-gram for Sequence-to-Sequence Pre-training](https://arxiv.org/abs/2001.04063v2). arXiv:2001.04063v2, 2020. The source code is [ProphetNet](https://github.com/microsoft/ProphetNet).
1. Itsumi Saito, Kyosuke Nishida, Kosuke Nishida, Atsushi Otsuka, Hisako Asano, Junji Tomita, Hiroyuki Shindo, Yuji Matsumoto. [Length-controllable Abstractive Summarization by Guiding with Summary Prototype](https://arxiv.org/abs/2001.07331v1). arXiv:2001.07331v1, 2020.
1. Dongling Xiao, Han Zhang, Yukun Li, Yu Sun, Hao Tian, Hua Wu, Haifeng Wang. [ERNIE-GEN: An Enhanced Multi-Flow Pre-training and Fine-tuning Framework for Natural Language Generation](https://arxiv.org/abs/2001.11314v3). arXiv:2001.11314v3, 2020. The source code is [ernie-gen](https://github.com/PaddlePaddle/ERNIE/tree/repro/ernie-gen).
1. Ahmed Magooda, Diane Litman. [Abstractive Summarization for Low Resource Data using Domain Transfer and Data Synthesis](https://arxiv.org/abs/2002.03407v1). arXiv:2002.03407v1, FLAIRS33 2020.
1. Wonjin Yoon, Yoon Sun Yeo, Minbyul Jeong, Bong-Jun Yi, Jaewoo Kang. [Learning by Semantic Similarity Makes Abstractive Summarization Better](https://arxiv.org/abs/2002.07767v1). arXiv:2002.07767v1, 2020.
1. Ritesh Sarkhel, Moniba Keymanesh, Arnab Nandi, Srinivasan Parthasarathy. [Transfer Learning for Abstractive Summarization at Controllable Budgets](https://arxiv.org/abs/2002.07845v1). arXiv:2002.07845v1, 2020.
1. Thomas Scialom, Paul-Alexis Dray, Sylvain Lamprier, Benjamin Piwowarski, Jacopo Staiano. [Discriminative Adversarial Search for Abstractive Summarization](https://arxiv.org/abs/2002.10375v1). arXiv:2002.10375v1, 2020.
1. Wei-Fan Chen, Shahbaz Syed, Benno Stein, Matthias Hagen, Martin Potthast. [Abstractive Snippet Generation](https://arxiv.org/abs/2002.10782v2). arXiv:2002.10782v2, 2020.
1. Satyaki Chakraborty, Xinya Li, Sayak Chakraborty. [A more abstractive summarization model](https://arxiv.org/abs/2002.10959v1). arXiv:2002.10959v1, 2020.
1. Chenguang Zhu, William Hinthorn, Ruochen Xu, Qingkai Zeng, Michael Zeng, Xuedong Huang, Meng Jiang. [Boosting Factual Correctness of Abstractive Summarization](https://arxiv.org/abs/2003.08612v4). arXiv:2003.08612v4, 2020.
1. Dmitrii Aksenov, Julián Moreno-Schneider, Peter Bourgonje, Robert Schwarzenberg, Leonhard Hennig, Georg Rehm. [Abstractive Text Summarization based on Language Model Conditioning and Locality Modeling](https://arxiv.org/abs/2003.13027v1). arXiv:2003.13027v1, 2020.
1. Itsumi Saito, Kyosuke Nishida, Kosuke Nishida, Junji Tomita. [Abstractive Summarization with Combination of Pre-trained Sequence-to-Sequence and Saliency Models](https://arxiv.org/abs/2003.13028v1). arXiv:2003.13028v1, 2020.
1. Amr M. Zaki, Mahmoud I. Khalil, Hazem M. Abbas. [Amharic Abstractive Text Summarization](https://arxiv.org/abs/2003.13721v1). arXiv:2003.13721v1, 2020.
1. Piji Li, Lidong Bing, Zhongyu Wei, Wai Lam. [Salience Estimation with Multi-Attention Learning for Abstractive Text Summarization](https://arxiv.org/abs/2004.03589v1). arXiv:2004.03589v1, 2020.
1. Tanya Chowdhury, Sachin Kumar, Tanmoy Chakraborty. [Neural Abstractive Summarization with Structural Attention](https://arxiv.org/abs/2004.09739v1). arXiv:2004.09739v1, IJCAI 2020.
1. Zhanghao Wu, Zhijian Liu, Ji Lin, Yujun Lin, Song Han. [Lite Transformer with Long-Short Range Attention](https://arxiv.org/abs/2004.11886v1). arXiv:2004.11886v1, ICLR 2020. The source code is [lite-transformer](https://github.com/mit-han-lab/lite-transformer).
1. Wei Li, Xinyan Xiao, Jiachen Liu, Hua Wu, Haifeng Wang, Junping Du. [Leveraging Graph to Improve Abstractive Multi-Document Summarization](https://arxiv.org/abs/2005.10043v1). arXiv:2005.10043v1, ACL 2020.
1. Virapat Kieuvongngam, Bowen Tan, Yiming Niu. [Automatic Text Summarization of COVID-19 Medical Research Articles using BERT and GPT-2](https://arxiv.org/abs/2006.01997v1). arXiv:2006.01997v1, 2020.
1. Logan Lebanoff, John Muchovej, Franck Dernoncourt, Doo Soon Kim, Lidan Wang, Walter Chang, Fei Liu. [Understanding Points of Correspondence between Sentences for Abstractive Summarization](https://arxiv.org/abs/2006.05621v1). arXiv:2006.05621v1, 2020. The source code is [points-of-correspondence](https://github.com/ucfnlp/points-of-correspondence).
1. Beliz Gunel, Chenguang Zhu, Michael Zeng, Xuedong Huang. [Mind The Facts: Knowledge-Boosted Coherent Abstractive Text Summarization](https://arxiv.org/abs/2006.15435v1). arXiv:2006.15435v1, NeurIPS 2019.
1. Philippe Laban, Andrew Hsi, John Canny, Marti A. Hearst. [The Summary Loop: Learning to Write Abstractive Summaries Without Examples](https://www.aclweb.org/anthology/2020.acl-main.460/). ACL, July 2020. The source code is [summary_loop](https://github.com/cannylab/summary_loop).


### Text Summarization

1. Eduard Hovy and Chin-Yew Lin. [Automated text summarization and the summarist system](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/tipster-proc-hovy-lin-final.pdf). In Proceedings of a Workshop on Held at Baltimore, Maryland, ACL, 1998.
2. Eduard Hovy and Chin-Yew Lin. [Automated Text Summarization in SUMMARIST](https://www.isi.edu/natural-language/people/hovy/papers/98hovylin-summarist.pdf). In Advances in Automatic Text Summarization, 1999.
3. Dipanjan Das and Andre F.T. Martins. [A survey on automatic text summarization](https://wtlab.um.ac.ir/images/e-library/text_summarization/A%20Survey%20on%20Automatic%20Text%20Summarization.pdf). Technical report, CMU, 2007
4. J. Leskovec, L. Backstrom, J. Kleinberg. [Meme-tracking and the Dynamics of the News Cycle](http://www.memetracker.org). ACM SIGKDD Intl. Conf. on Knowledge Discovery and Data Mining, 2009.
5. Ryang, Seonggi, and Takeshi Abekawa. "[Framework of automatic text summarization using reinforcement learning](http://dl.acm.org/citation.cfm?id=2390980)." In Proceedings of the 2012 Joint Conference on Empirical Methods in Natural Language Processing and Computational Natural Language Learning, pp. 256-265. Association for Computational Linguistics, 2012. [not neural-based methods]
6. King, Ben, Rahul Jha, Tyler Johnson, Vaishnavi Sundararajan, and Clayton Scott. "[Experiments in Automatic Text Summarization Using Deep Neural Networks](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.459.8775&rep=rep1&type=pdf)." Machine Learning (2011).
7. Liu, Yan, Sheng-hua Zhong, and Wenjie Li. "[Query-Oriented Multi-Document Summarization via Unsupervised Deep Learning](http://www.aaai.org/ocs/index.php/AAAI/AAAI12/paper/view/5058/5322)." AAAI. 2012.
8. He, Zhanying, Chun Chen, Jiajun Bu, Can Wang, Lijun Zhang, Deng Cai, and Xiaofei He. "[Document Summarization Based on Data Reconstruction](http://cs.nju.edu.cn/zlj/pdf/AAAI-2012-He.pdf)." In AAAI. 2012.
9. Mohsen Pourvali, Mohammad Saniee Abadeh. [Automated Text Summarization Base on Lexicales Chain and graph Using of WordNet and Wikipedia Knowledge Base](https://arxiv.org/abs/1203.3586v1). arXiv:1203.3586, 2012.
10. PadmaPriya, G., and K. Duraiswamy. [An Approach For Text Summarization Using Deep Learning Algorithm](http://thescipub.com/PDF/jcssp.2014.1.9.pdf). Journal of Computer Science 10, no. 1 (2013): 1-9.
11. Rushdi Shams, M.M.A. Hashem, Afrina Hossain, Suraiya Rumana Akter, Monika Gope. [Corpus-based Web Document Summarization using Statistical and Linguistic Approach](https://arxiv.org/abs/1304.2476v1). arXiv:1304.2476, Procs. of the IEEE International Conference on Computer and Communication Engineering (ICCCE10), pp. 115-120, Kuala Lumpur, Malaysia, May 11-13, (2010).
12. Juan-Manuel Torres-Moreno. [Beyond Stemming and Lemmatization: Ultra-stemming to Improve Automatic Text Summarization](https://arxiv.org/abs/1209.3126). arXiv:1209.3126, 2012.
13. Rioux, Cody, Sadid A. Hasan, and Yllias Chali. [Fear the REAPER: A System for Automatic Multi-Document Summarization with Reinforcement Learning](http://emnlp2014.org/papers/pdf/EMNLP2014075.pdf). In EMNLP, pp. 681-690. 2014.[not neural-based methods]
14. Fatma El-Ghannam, Tarek El-Shishtawy. [Multi-Topic Multi-Document Summarizer](https://arxiv.org/abs/1401.0640v1). arXiv:1401.0640, 2014.
15. Denil, Misha, Alban Demiraj, and Nando de Freitas. [Extraction of Salient Sentences from Labelled Documents](http://arxiv.org/abs/1412.6815). arXiv:1412.6815,  2014.
16. Denil, Misha, Alban Demiraj, Nal Kalchbrenner, Phil Blunsom, and Nando de Freitas.[Modelling, Visualising and Summarising Documents with a Single Convolutional Neural Network](http://arxiv.org/abs/1406.3830). arXiv:1406.3830, 2014.
17. Cao, Ziqiang, Furu Wei, Li Dong, Sujian Li, and Ming Zhou. [Ranking with Recursive Neural Networks and Its Application to Multi-document Summarization](http://gana.nlsde.buaa.edu.cn/~lidong/aaai15-rec_sentence_ranking.pdf). AAAI, 2015.
18. Fei Liu, Jeffrey Flanigan, Sam Thomson, Norman Sadeh, and Noah A. Smith. [Toward Abstractive Summarization Using Semantic Representations](http://www.cs.cmu.edu/~nasmith/papers/liu+flanigan+thomson+sadeh+smith.naacl15.pdf). NAACL, 2015.
19. Wenpeng Yin， Yulong Pei. Optimizing Sentence Modeling and Selection for Document Summarization. IJCAI, 2015.
20. Liu, He, Hongliang Yu, and Zhi-Hong Deng. [Multi-Document Summarization Based on Two-Level Sparse Representation Model](http://www.cis.pku.edu.cn/faculty/system/dengzhihong/papers/AAAI%202015_Multi-Document%20Summarization%20Based%20on%20Two-Level%20Sparse%20Representation%20Model.pdf). In Twenty-Ninth AAAI Conference on Artificial Intelligence. 2015.
21. Jin-ge Yao, Xiaojun Wan and Jianguo Xiao. [Compressive Document Summarization via Sparse Optimization](http://ijcai.org/Proceedings/15/Papers/198.pdf). IJCAI, 2015.
22. Piji Li, Lidong Bing, Wai Lam, Hang Li, and Yi Liao. [Reader-Aware Multi-Document Summarization via Sparse Coding](http://arxiv.org/abs/1504.07324). arXiv:1504.07324,  IJCAI, 2015.
23. Marta Aparício, Paulo Figueiredo, Francisco Raposo, David Martins de Matos, Ricardo Ribeiro, Luís Marujo. [Summarization of Films and Documentaries Based on Subtitles and Scripts](https://arxiv.org/abs/1506.01273v3). arXiv:1506.01273, 2015.
24. Luís Marujo, Ricardo Ribeiro, David Martins de Matos, João P. Neto, Anatole Gershman, Jaime Carbonell. [Extending a Single-Document Summarizer to Multi-Document: a Hierarchical Approach](https://arxiv.org/abs/1507.02907v1). arXiv:1507.02907, 2015.
25. Xiaojun Wan, Yansong Feng and Weiwei Sun. [Automatic Text Generation: Research Progress and Future Trends](http://www.icst.pku.edu.cn/lcwm/wanxj/files/TextGenerationSurvey.pdf). Book Chapter in CCF 2014-2015 Annual Report on Computer Science and Technology in China (In Chinese), 2015.
26. Xiaojun Wan, Ziqiang Cao, Furu Wei, Sujian Li, Ming Zhou. [Multi-Document Summarization via Discriminative Summary Reranking](https://arxiv.org/abs/1507.02062v1).     arXiv:1507.02062, 2015.
27. Gulcehre, Caglar, Sungjin Ahn, Ramesh Nallapati, Bowen Zhou, and Yoshua Bengio. [Pointing the Unknown Words](http://arxiv.org/abs/1603.08148). arXiv:1603.08148, 2016.
28. Jiatao Gu, Zhengdong Lu, Hang Li, Victor O.K. Li. [Incorporating Copying Mechanism in Sequence-to-Sequence Learning](https://arxiv.org/abs/1603.06393). arXiv:1603.06393, ACL, 2016.
    - They addressed an important problem in sequence-to-sequence (Seq2Seq) learning referred to as copying, in which certain segments in the input sequence are selectively replicated in the output sequence. In this paper, they incorporated copying into neural network-based Seq2Seq learning and propose a new model called CopyNet with encoder-decoder structure. CopyNet can nicely integrate the regular way of word generation in the decoder with the new copying mechanism which can choose sub-sequences in the input sequence and put them at proper places in the output sequence.
29. Jianmin Zhang, Jin-ge Yao and Xiaojun Wan. [Toward constructing sports news from live text commentary](http://www.icst.pku.edu.cn/lcwm/wanxj/files/acl16_sports.pdf). In Proceedings of ACL, 2016.
30. Ziqiang Cao, Wenjie Li, Sujian Li, Furu Wei. "[AttSum: Joint Learning of Focusing and Summarization with Neural Attention](http://arxiv.org/abs/1604.00125)".  arXiv:1604.00125, 2016
31. Ayana, Shiqi Shen, Yu Zhao, Zhiyuan Liu and Maosong Sun. [Neural Headline Generation with Sentence-wise Optimization](https://arxiv.org/abs/1604.01904). arXiv:1604.01904, 2016.
32. Ayana, Shiqi Shen, Zhiyuan Liu and Maosong Sun. [Neural Headline Generation with Minimum Risk Training](https://128.84.21.199/abs/1604.01904v1). 2016.
33. Lu Wang, Hema Raghavan, Vittorio Castelli, Radu Florian, Claire Cardie. [A Sentence Compression Based Framework to Query-Focused Multi-Document Summarization](https://arxiv.org/abs/1606.07548v1). arXiv:1606.07548, 2016.
34. Milad Moradi, Nasser Ghadiri. [Different approaches for identifying important concepts in probabilistic biomedical text summarization](https://arxiv.org/abs/1605.02948v3). arXiv:1605.02948, 2016.
35. Kikuchi, Yuta, Graham Neubig, Ryohei Sasano, Hiroya Takamura, and Manabu Okumura. [Controlling Output Length in Neural Encoder-Decoders](https://arxiv.org/abs/1609.09552). arXiv:1609.09552, 2016.
36. Qian Chen, Xiaodan Zhu, Zhenhua Ling, Si Wei and Hui Jiang. [Distraction-Based Neural Networks for Document Summarization](https://arxiv.org/abs/1610.08462). arXiv:1610.08462, IJCAI, 2016.
37. Wang, Lu, and Wang Ling. [Neural Network-Based Abstract Generation for Opinions and Arguments](http://www.ccs.neu.edu/home/luwang/papers/NAACL2016.pdf). NAACL, 2016.
38. Yishu Miao, Phil Blunsom.  [Language as a Latent Variable: Discrete Generative Models for Sentence Compression](http://arxiv.org/abs/1609.07317).  EMNLP, 2016.
39. Takase, Sho, Jun Suzuki, Naoaki Okazaki, Tsutomu Hirao, and Masaaki Nagata. [Neural headline generation on abstract meaning representation](https://www.aclweb.org/anthology/D/D16/D16-1112.pdf).  EMNLP, 1054-1059, 2016.
40. Wenyuan Zeng, Wenjie Luo, Sanja Fidler, Raquel Urtasun.  [Efficient Summarization with Read-Again and Copy Mechanism](https://arxiv.org/abs/1611.03382). arXiv:1611.03382, 2016.
41. Ziqiang Cao, Wenjie Li, Sujian Li, Furu Wei. [Improving Multi-Document Summarization via Text Classification](https://arxiv.org/abs/1611.09238v1). arXiv:1611.09238, 2016.
42. Hongya Song, Zhaochun Ren, Piji Li, Shangsong Liang, Jun Ma, and Maarten de Rijke. [Summarizing Answers in Non-Factoid Community Question-Answering](http://dl.acm.org/citation.cfm?id=3018704). In WSDM 2017: The 10th International Conference on Web Search and Data Mining, 2017.
43. Piji Li, Zihao Wang, Wai Lam, Zhaochun Ren, Lidong Bing.  [Salience Estimation via Variational Auto-Encoders for Multi-Document Summarization](https://aaai.org/ocs/index.php/AAAI/AAAI17/paper/view/14613). In AAAI, 2017.
44. Yinfei Yang, Forrest Sheng Bao, Ani Nenkova. [Detecting (Un)Important Content for Single-Document News Summarization](https://arxiv.org/abs/1702.07998v1). arXiv:1702.07998, 2017.
45. Rui Meng, Sanqiang Zhao, Shuguang Han, Daqing He, Peter Brusilovsky, Yu Chi. [Deep Keyphrase Generation](https://arxiv.org/abs/1704.06879v1). arXiv:1704.06879, 2017. The source code written in Python is [seq2seq-keyphrase](https://github.com/memray/seq2seq-keyphrase).
46. Abigail See, Peter J. Liu and Christopher D. Manning. [Get To The Point: Summarization with Pointer-Generator Networks](https://arxiv.org/abs/1704.04368). ACL, 2017. The souce code is [pointer-generator](https://github.com/abisee/pointer-generator).
47. Qingyu Zhou, Nan Yang, Furu Wei and Ming Zhou. [Selective Encoding for Abstractive Sentence Summarization](https://arxiv.org/abs/1704.07073). arXiv:1704.07073, ACL, 2017.
48. Jin-ge Yao, Xiaojun Wan and Jianguo Xiao. [Recent Advances in Document Summarization](http://www.icst.pku.edu.cn/lcwm/wanxj/files/summ_survey_draft.pdf). KAIS, survey paper, 2017.
49. Pranay Mathur, Aman Gill and Aayush Yadav. [Text Summarization in Python: Extractive vs. Abstractive techniques revisited](https://rare-technologies.com/text-summarization-in-python-extractive-vs-abstractive-techniques-revisited/#text_summarization_in_python). 2017.
    - They compared modern extractive methods like LexRank, LSA, Luhn and Gensim’s existing TextRank summarization module on the [Opinosis dataset](http://kavita-ganesan.com/opinosis-opinion-dataset) of 51 (article, summary) pairs. They also had a try with an abstractive technique using Tensorflow’s algorithm [textsum](https://github.com/tensorflow/models/tree/master/textsum), but didn’t obtain good results due to its extremely high hardware demands (7000 GPU hours).
50. Arman Cohan, Nazli Goharian. [Scientific Article Summarization Using Citation-Context and Article's Discourse Structure](https://arxiv.org/abs/1704.06619v1). arXiv:1704.06619, EMNLP, 2015.
51. Shuming Ma, Xu Sun, Jingjing Xu, Houfeng Wang, Wenjie Li, Qi Su. [Improving Semantic Relevance for Sequence-to-Sequence Learning of Chinese Social Media Text Summarization](https://arxiv.org/abs/1706.02459). The source code written in Python is [SRB](https://github.com/lancopku/SRB).
52. Arman Cohan, Nazli Goharian. [Scientific document summarization via citation contextualization and scientific discourse](https://arxiv.org/abs/1706.03449v1). arXiv:1706.03449, 2017.
53. Michihiro Yasunaga, Rui Zhang, Kshitijh Meelu, Ayush Pareek, Krishnan Srinivasan, Dragomir Radev. [Graph-based Neural Multi-Document Summarization](https://arxiv.org/abs/1706.06681v3). arXiv:1706.06681, CoNLL, 2017.
54. Abeed Sarker, Diego Molla, Cecile Paris. [Automated text summarisation and evidence-based medicine: A survey of two domains](https://arxiv.org/abs/1706.08162v1). arXiv:1706.08162, 2017.
55. Mehdi Allahyari, Seyedamin Pouriyeh, Mehdi Assefi, Saeid Safaei, Elizabeth D. Trippe, Juan B. Gutierrez, Krys Kochut. [Text Summarization Techniques: A Brief Survey](https://arxiv.org/abs/1707.02268). arXiv:1707.02268, 2017.
56. Demian Gholipour Ghalandari. [Revisiting the Centroid-based Method: A Strong Baseline for Multi-Document Summarization](https://arxiv.org/abs/1708.07690v1). arXiv:1708.07690, EMNLP, 2017.
57. Shuming Ma, Xu Sun. [A Semantic Relevance Based Neural Network for Text Summarization and Text Simplification](https://arxiv.org/abs/1710.02318v1). arXiv:1710.02318, 2017. The source code written in Python is [SRB](https://github.com/lancopku/SRB).
58. Kaustubh Mani, Ishan Verma, Lipika Dey. [Multi-Document Summarization using Distributed Bag-of-Words Model](https://arxiv.org/abs/1710.02745v1). arXiv:1710.02745, 2017.
59. Liqun Shao, Hao Zhang, Ming Jia, Jie Wang. [Efficient and Effective Single-Document Summarizations and A Word-Embedding Measurement of Quality](https://arxiv.org/abs/1710.00284v1). arXiv:1710.00284, KDIR, 2017.
60. Mohammad Ebrahim Khademi, Mohammad Fakhredanesh, Seyed Mojtaba Hoseini. [Conceptual Text Summarizer: A new model in continuous vector space](https://arxiv.org/abs/1710.10994v2). arXiv:1710.10994, 2017.
61. Jingjing Xu. [Improving Social Media Text Summarization by Learning Sentence Weight Distribution](https://arxiv.org/abs/1710.11332v1). arXiv:1710.11332, 2017.
62. Peter J. Liu, Mohammad Saleh, Etienne Pot, Ben Goodrich, Ryan Sepassi, Lukasz Kaiser, Noam Shazeer. [Generating Wikipedia by Summarizing Long Sequences](https://arxiv.org/abs/1801.10198v1). arXiv:1801.10198, 2018.
63. Parth Mehta, Prasenjit Majumder. [Content based Weighted Consensus Summarization](https://arxiv.org/abs/1802.00946v1). arXiv:1802.00946, 2018.
64. Mayank Chaudhari, Aakash Nelson Mattukoyya. [Tone Biased MMR Text Summarization](https://arxiv.org/abs/1802.09426v2). arXiv:1802.09426, 2018.
65. Divyanshu Daiya, Anukarsh Singh, Mukesh Jadon. [Using Statistical and Semantic Models for Multi-Document Summarization](https://arxiv.org/abs/1805.04579v2). arXiv:1805.04579, 2018.
66. Wan-Ting Hsu, Chieh-Kai Lin, Ming-Ying Lee, Kerui Min, Jing Tang, Min Sun. [A Unified Model for Extractive and Abstractive Summarization using Inconsistency Loss](https://arxiv.org/abs/1805.06266v2).arXiv:1805.06266, ACL 2018.
67. Pei Guo, Connor Anderson, Kolten Pearson, Ryan Farrell. [Neural Network Interpretation via Fine Grained Textual Summarization](https://arxiv.org/abs/1805.08969v2). arXiv:1805.08969, 2018.
68. Kamal Al-Sabahi, Zhang Zuping, Yang Kang. [Latent Semantic Analysis Approach for Document Summarization Based on Word Embeddings](https://arxiv.org/abs/1807.02748v1). arXiv:1807.02748, KSII Transactions on Internet and Information Systems, 2018.
69. Chandra Khatri, Gyanit Singh, Nish Parikh. [Abstractive and Extractive Text Summarization using Document Context Vector and Recurrent Neural Networks](https://arxiv.org/abs/1807.08000v2). arXiv:1807.08000v2, ACM KDD 2018 Deep Learning Day, 2018.
70. Ziqiang Cao, Wenjie Li, Sujian Li, Furu Wei. [Retrieve, Rerank and Rewrite: Soft Template Based Neural Summarization](https://www.aclweb.org/anthology/P18-1015/). ACL, July 2018.
71. Yang Zhao, Zhiyuan Luo, Akiko Aizawa. [A Language Model based Evaluator for Sentence Compression](https://www.aclweb.org/anthology/P18-2028/). ACL, July 2018. The source code is [code4sc](https://github.com/code4conference/code4sc).
72. Logan Lebanoff, Kaiqiang Song, Fei Liu. [Adapting the Neural Encoder-Decoder Framework from Single to Multi-Document Summarization](https://arxiv.org/abs/1808.06218v2). arXiv:1808.06218, 2018.
73. Shashi Narayan, Shay B. Cohen, Mirella Lapata. [Don't Give Me the Details, Just the Summary! Topic-Aware Convolutional Neural Networks for Extreme Summarization](https://arxiv.org/abs/1808.08745v1). arXiv:1808.08745, 2018.
74. Parth Mehta, Prasenjit Majumder. [Exploiting local and global performance of candidate systems for aggregation of summarization techniques](https://arxiv.org/abs/1809.02343v1). arXiv:1809.02343, 2018.
75. Ritwik Mishra and Tirthankar Gayen. "[Automatic Lossless-Summarization of News Articles with Abstract Meaning Representation](https://www.sciencedirect.com/science/article/pii/S1877050918314522)." Procedia Computer Science 135 (September 2018): 178-185.
76. Chi Zhang, Shagan Sah, Thang Nguyen, Dheeraj Peri, Alexander Loui, Carl Salvaggio, Raymond Ptucha. [Semantic Sentence Embeddings for Paraphrasing and Text Summarization](https://arxiv.org/abs/1809.10267v1). arXiv:1809.10267, IEEE GlobalSIP 2017 Conference, 2018.
77. Yaser Keneshloo, Naren Ramakrishnan, Chandan K. Reddy. [Deep Transfer Reinforcement Learning for Text Summarization](https://arxiv.org/abs/1810.06667v1). arXiv:1810.06667, 2018.
78. Elvys Linhares Pontes, Stéphane Huet, Juan-Manuel Torres-Moreno. [A Multilingual Study of Compressive Cross-Language Text Summarization](https://arxiv.org/abs/1810.10639v1). arXiv:1810.10639, 2018.
79. Patrick Fernandes, Miltiadis Allamanis, Marc Brockschmidt. [Structured Neural Summarization](https://arxiv.org/abs/1811.01824v2). arXiv:1811.01824v2, ICLR 2019.
80. Matthäus Kleindessner, Pranjal Awasthi, Jamie Morgenstern. [Fair k-Center Clustering for Data Summarization](https://arxiv.org/abs/1901.08628v2). arXiv:1901.08628v2, 2019.
81. Hadrien Van Lierde, Tommy W. S. Chow. [Query-oriented text summarization based on hypergraph transversals](https://arxiv.org/abs/1902.00672). arXiv:1902.00672v1, 2019.
82. Edward Moroshko, Guy Feigenblat, Haggai Roitman, David Konopnicki. [An Editorial Network for Enhanced Document Summarization](https://arxiv.org/abs/1902.10360v1). arXiv:1902.10360v1, 2019.
83. Erion Çano, Ondřej Bojar. [Keyphrase Generation: A Text Summarization Struggle](https://arxiv.org/abs/1904.00110v2). arXiv:1904.00110v2, 2019.
84. Abdelkrime Aries, Djamel eddine Zegour, Walid Khaled Hidouci. [Automatic text summarization: What has been done and what has to be done](https://arxiv.org/abs/1904.00688v1). arXiv:1904.00688v1, 2019.
85. Sho Takase, Naoaki Okazaki. [Positional Encoding to Control Output Sequence Length](https://arxiv.org/abs/1904.07418v1). arXiv:1904.07418v1, NAACL-HLT 2019. The source code is [control-length](https://github.com/takase/control-length).
86. Nataliya Shakhovska, Taras Cherna. [The method of automatic summarization from different sources](https://arxiv.org/abs/1905.02623v1). arXiv:1905.02623v1, 2019.
87. Alexios Gidiotis, Grigorios Tsoumakas. [Structured Summarization of Academic Publications](https://arxiv.org/abs/1905.07695v2). arXiv:1905.07695v2, 2019.
88. Yang Liu, Mirella Lapata. [Hierarchical Transformers for Multi-Document Summarization](https://arxiv.org/abs/1905.13164v1). arXiv:1905.13164v1, ACL 2019.
89. Hao Zheng, Mirella Lapata. [Sentence Centrality Revisited for Unsupervised Summarization](https://arxiv.org/abs/1906.03508v1). arXiv:1906.03508v1, ACL 2019.
90. Jianying Lin, Rui Liu, Quanye Jia. [Joint Lifelong Topic Model and Manifold Ranking for Document Summarization](https://arxiv.org/abs/1907.03224v1). arXiv:1907.03224v1, 2019.
91. Jiawei Zhou, Alexander M. Rush. [Simple Unsupervised Summarization by Contextual Matching](https://arxiv.org/abs/1907.13337v1). arXiv:1907.13337v1, 2019.
92. Milad Moradi, Nasser Ghadiri. [Text Summarization in the Biomedical Domain](https://arxiv.org/abs/1908.02285v1). arXiv:1908.02285v1, 2019.
93. Yang Liu, Mirella Lapata. [Text Summarization with Pretrained Encoders](https://arxiv.org/abs/1908.08345v2). arXiv:1908.08345v2, 2019. The source code is [PreSumm](https://github.com/nlpyang/PreSumm).
94. Yacine Jernite. [Unsupervised Text Summarization via Mixed Model Back-Translation](https://arxiv.org/abs/1908.08566v1). arXiv:1908.08566v1, 2019.
95. Varun Pandya. [Automatic Text Summarization of Legal Cases: A Hybrid Approach](https://arxiv.org/abs/1908.09119v1). arXiv:1908.09119v1, 2019.
96. Shai Erera, Michal Shmueli-Scheuer, Guy Feigenblat, Ora Peled Nakash, Odellia Boni, Haggai Roitman, Doron Cohen, Bar Weiner, Yosi Mass, Or Rivlin, Guy Lev, Achiya Jerbi, Jonathan Herzig, Yufang Hou, Charles Jochim, Martin Gleize, Francesca Bonin, David Konopnicki. [A Summarization System for Scientific Documents](https://arxiv.org/abs/1908.11152v1). arXiv:1908.11152v1, 2019.
97. Taehee Jung, Dongyeop Kang, Lucas Mentch, Eduard Hovy. [Earlier Isn't Always Better: Sub-aspect Analysis on Corpus and System Biases in Summarization](https://arxiv.org/abs/1908.11723v1). arXiv:1908.11723v1, EMNLP 2019.
98. Junnan Zhu, Qian Wang, Yining Wang, Yu Zhou, Jiajun Zhang, Shaonan Wang, Chengqing Zong. [NCLS: Neural Cross-Lingual Summarization](https://arxiv.org/abs/1909.00156v1). arXiv:1909.00156v1, 2019.
99. Ruqian Lu, Shengluan Hou, Chuanqing Wang, Yu Huang, Chaoqun Fei, Songmao Zhang. [Attributed Rhetorical Structure Grammar for Domain Text Summarization](https://arxiv.org/abs/1909.00923v1). arXiv:1909.00923v1, 2019.
100. Michihiro Yasunaga, Jungo Kasai, Rui Zhang, Alexander R. Fabbri, Irene Li, Dan Friedman, Dragomir R. Radev. [ScisummNet: A Large Annotated Dataset and Content-Impact Models for Scientific Paper Summarization with Citation Networks](https://arxiv.org/abs/1909.01716v1). arXiv:1909.01716v1, 2019.
101. Daniel M. Ziegler, Nisan Stiennon, Jeffrey Wu, Tom B. Brown, Alec Radford, Dario Amodei, Paul Christiano, Geoffrey Irving. [Fine-Tuning Language Models from Human Preferences](https://arxiv.org/abs/1909.08593v2). arXiv:1909.08593v2, 2019. [lm-human-preferences](https://github.com/openai/lm-human-preferences) contains code for the paper.
102. Khanh Nguyen, Hal Daumé III. [Global Voices: Crossing Borders in Automatic News Summarization](https://arxiv.org/abs/1910.00421v4). arXiv:1910.00421v4, EMNLP 2019.
103. Shengluan Hou, Ruqian Lu. [Knowledge-guided Unsupervised Rhetorical Parsing for Text Summarization](https://arxiv.org/abs/1910.05915v1).  arXiv:1910.05915v1, 2019.
104. Xingbang Liu, Janyl Jumadinova. [Automated Text Summarization for the Enhancement of Public Services](https://arxiv.org/abs/1910.10490).  arXiv:1910.10490v1, 2019.
105. Chenguang Zhu, Ziyi Yang, Robert Gmyr, Michael Zeng, Xuedong Huang. [Make Lead Bias in Your Favor: A Simple and Effective Method for News Summarization](https://arxiv.org/abs/1912.11602v2). arXiv:1912.11602v2, 2019.
106. Hidetaka Kamigaito, Manabu Okumura. [Syntactically Look-Ahead Attention Network for Sentence Compression](https://arxiv.org/abs/2002.01145v2). arXiv:2002.01145v2, AAAI 2020. The source code is [SLAHAN](https://github.com/kamigaito/SLAHAN).
107. Hangbo Bao, Li Dong, Furu Wei, Wenhui Wang, Nan Yang, Xiaodong Liu, Yu Wang, Songhao Piao, Jianfeng Gao, Ming Zhou, Hsiao-Wuen Hon. [UniLMv2: Pseudo-Masked Language Models for Unified Language Model Pre-Training](https://arxiv.org/abs/2002.12804v1). arXiv:2002.12804v1, 2020. The source code is [unilm](https://github.com/microsoft/unilm).
108. Wei-Hung Weng, Yu-An Chung, Schrasing Tong. [Clinical Text Summarization with Syntax-Based Negation and Semantic Concept Identification](https://arxiv.org/abs/2003.00353v1). arXiv:2003.00353v1, 2020.
109. Vidhisha Balachandran, Artidoro Pagnoni, Jay Yoon Lee, Dheeraj Rajagopal, Jaime Carbonell, Yulia Tsvetkov. [StructSum: Incorporating Latent and Explicit Sentence Dependencies for Single Document Summarization](https://arxiv.org/abs/2003.00576v1). arXiv:2003.00576v1, 2020.
110. Haiyang Xu, Yun Wang, Kun Han, Baochang Ma, Junwen Chen, Xiangang Li. [Selective Attention Encoders by Syntactic Graph Convolutional Networks for Document Summarization](https://arxiv.org/abs/2003.08004v1). arXiv:2003.08004v1, ICASSP 2020.
111. Haiyang Xu, Yahao He, Kun Han, Junwen Chen, Xiangang Li. [Learning Syntactic and Dynamic Selective Encoding for Document Summarization](https://arxiv.org/abs/2003.11173v1). arXiv:2003.11173v1, IJCNN 2019.
112. Yanyan Zou, Xingxing Zhang, Wei Lu, Furu Wei, Ming Zhou. [STEP: Sequence-to-Sequence Transformer Pre-training for Document Summarization](https://arxiv.org/abs/2004.01853v1). arXiv:2004.01853v1, 2020.
113. Alexios Gidiotis, Grigorios Tsoumakas. [A Divide-and-Conquer Approach to the Summarization of Long Documents](https://arxiv.org/abs/2004.06190v2). arXiv:2004.06190v2, 2020.
114. Isabel Cachola, Kyle Lo, Arman Cohan, Daniel S. Weld. [TLDR: Extreme Summarization of Scientific Documents](https://arxiv.org/abs/2004.15011v2). arXiv:2004.15011v2, 2020.
115. Sho Takase, Sosuke Kobayashi. [All Word Embeddings from One Embedding](https://arxiv.org/abs/2004.12073v2). arXiv:2004.12073v2, 2020. The source code is [alone_seq2seq](https://github.com/takase/alone_seq2seq).
116. Luyang Huang, Lingfei Wu, Lu Wang. [Knowledge Graph-Augmented Abstractive Summarization with Semantic-Driven Cloze Reward](https://arxiv.org/abs/2005.01159v1). arXiv:2005.01159v1, ACL 2020.
117. Raphael Schumann, Lili Mou, Yao Lu, Olga Vechtomova, Katja Markert. [Discrete Optimization for Unsupervised Sentence Summarization with Word-Level Extraction](https://arxiv.org/abs/2005.01791v1). arXiv:2005.01791v1, ACL 2020.
118. Shen Gao, Xiuying Chen, Zhaochun Ren, Dongyan Zhao, Rui Yan. [From Standard Summarization to New Tasks and Beyond: Summarization with Manifold Information](https://arxiv.org/abs/2005.04684v1). arXiv:2005.04684v1, IJCAI 2020.
119. Pirmin Lemberger. [Deep Learning Models for Automatic Summarization](https://arxiv.org/abs/2005.11988v1). arXiv:2005.11988v1, 2020.
120. Vladislav Tretyak, Denis Stepanov. [Combination of abstractive and extractive approaches for summarization of long scientific texts](https://arxiv.org/abs/2006.05354v2). arXiv:2006.05354v2, 2020.
121. Yao Zhao, Mohammad Saleh, Peter J.Liu. [SEAL: Segment-wise Extractive-Abstractive Long-form Text Summarization](https://arxiv.org/abs/2006.10213v1). arXiv:2006.10213v1, 2020.
122. Zi-Yi Dou, Sachin Kumar, Yulia Tsvetkov. [A Deep Reinforced Model for Zero-Shot Cross-Lingual Summarization with Bilingual Semantic Similarity Rewards](https://arxiv.org/abs/2006.15454v1). arXiv:2006.15454v1, 2020.
123. Roger Barrull, Jugal Kalita. [Abstractive and mixed summarization for long-single documents](https://arxiv.org/abs/2007.01918v1). arXiv:2007.01918v1, 2020.
124. Paul Tardy, David Janiszek, Yannick Estève, Vincent Nguyen. [Align then Summarize: Automatic Alignment Methods for Summarization Corpus Creation](https://arxiv.org/abs/2007.07841v1). arXiv:2007.07841v1, LREC 2020.
125. L. Elisa Celis, Vijay Keswani. [Dialect Diversity in Text Summarization on Twitter](https://arxiv.org/abs/2007.07860v1). arXiv:2007.07860v1, 2020.
126. Jinming Zhao, Ming Liu, Longxiang Gao, Yuan Jin, Lan Du, He Zhao, He Zhang, Gholamreza Haffari. [SummPip: Unsupervised Multi-Document Summarization with Sentence Graph Compression](https://arxiv.org/abs/2007.08954v2). arXiv:2007.08954v2, SIGIR 2020.
127. Nisan Stiennon, Long Ouyang, Jeff Wu, Daniel M. Ziegler, Ryan Lowe, Chelsea Voss, Alec Radford, Dario Amodei, Paul Christiano. [Learning to summarize from human feedback](https://arxiv.org/abs/2009.01325v2). arXiv:2009.01325v2. [summarize-from-feedback](https://github.com/openai/summarize-from-feedback) contains code to run the models, including the supervised baseline, the trained reward model, and the RL fine-tuned policy. See also the [blog post](https://www.openai.com/blog/learning-to-summarize-with-human-feedback/).

### Chinese Text Summarization

1. Mao Song Sun. [Natural Language Processing Based on Naturally Annotated Web Resources](http://www.thunlp.org/site2/images/stories/files/2011_zhongwenxinxixuebao_sms.pdf). Journal of Chinese Information Processing, 2011.
2. Baotian Hu, Qingcai Chen and Fangze Zhu. [LCSTS: A Large Scale Chinese Short Text Summarization Dataset](https://arxiv.org/abs/1506.05865). 2015.
   - They constructed a large-scale Chinese short text summarization dataset constructed from the Chinese microblogging website Sina Weibo, which is released to [the public](http://icrc.hitsz.edu.cn/Article/show/139.html). Then they performed GRU-based encoder-decoder method on it to generate summary. They took the whole short text as one sequence, this may not be very reasonable, because most of short texts contain several sentences.
   - LCSTS contains 2,400,591 (short text, summary) pairs as the training set and 1,106  pairs as the test set.
   - All the models are trained on the GPUs tesla M2090 for about one week.
   - The results show that the RNN with context outperforms RNN without context on both character and word based input.
   - Moreover, the performances of the character-based input outperform the word-based input.
3. Bingzhen Wei, Xuancheng Ren, Xu Sun, Yi Zhang, Xiaoyan Cai, Qi Su. [Regularizing Output Distribution of Abstractive Chinese Social Media Text Summarization for Improved Semantic Consistency](https://arxiv.org/abs/1805.04033v1). arXiv:1805.04033, 2018.
4. [LancoSum](https://github.com/lancopku/LancoSum) provides a toolkit for abstractive summarization, which can achieve the SOTA performance.
   * Shuming Ma, Xu Sun, Wei Li, Sujian Li, Wenjie Li, Xuancheng Ren. [Query and Output: Generating Words by Querying Distributed Word Representations for Paraphrase Generation](https://arxiv.org/abs/1803.01465v3). arXiv:1803.01465v3, NAACL HLT 2018.
   * Junyang Lin, Xu Sun, Shuming Ma, Qi Su. [Global Encoding for Abstractive Summarization](https://arxiv.org/abs/1805.03989v2). arXiv:1805.03989v2, ACL 2018. The source code written in Python is [Global-Encoding](https://github.com/lancopku/Global-Encoding).
   * Shuming Ma, Xu Sun, Junyang Lin and Houfeng Wang. [Autoencoder as Assistant Supervisor: Improving Text Representation for Chinese Social Media Text Summarization](https://arxiv.org/abs/1805.04869v1). arXiv:1805.04869, ACL 2018. The source code written in Python is [superAE](https://github.com/lancopku/superAE).


### Program Source Code Summarization

1. Najam Nazar, Yan Hu, and He Jiang.
[Summarizing Software Artifacts: A Literature Review](http://oscar-lab.org/paper/jcst_16.pdf). Journal of Computer Science and Technology, 2016, 31, 883-909.
     * This paper presents a literature review in the field of summarizing software artifacts, focusing on bug reports, source code, mailing lists and developer discussions artifacts.
2. [paperswithcode](https://paperswithcode.com/task/code-summarization) a website that collects research papers in computer science with together with their code artifacts, this link is to so a section on source code summarization.
3. Laura Moreno, Andrian Marcus.
[Automatic Software Summarization: The State of the Art](https://dl.acm.org/citation.cfm?doid=3183440.3183464). (ICSE '18) Proceedings of the 40th International Conference on Software Engineering: Companion Proceeedings, pp. 530-531
    * Another review paper, but much shorter.
1. Alexander LeClair, Sakib Haque, Lingfei Wu, Collin McMillan. [Improved Code Summarization via a Graph Neural Network](https://arxiv.org/abs/2004.02843v2). arXiv:2004.02843v2, 2020.
1. Wasi Uddin Ahmad, Saikat Chakraborty, Baishakhi Ray, Kai-Wei Chang. [A Transformer-based Approach for Source Code Summarization](https://arxiv.org/abs/2005.00653v1). arXiv:2005.00653v1, ACL 2020.
1. Shangqing Liu, Yu Chen, Xiaofei Xie, Jing Kai Siow, Yang Liu. [Automatic Code Summarization via Multi-dimensional Semantic Fusing in GNN](https://arxiv.org/abs/2006.05405v1). arXiv:2006.05405v1. 2020.


### Entity Summarization

1. Dongjun Wei, Yaxin Liu, Fuqing Zhu, Liangjun Zang, Wei Zhou, Jizhong Han, Songlin Hu. [ESA: Entity Summarization with Attention](https://arxiv.org/abs/1905.10625v4). arXiv:1905.10625v4, 2019.
1. Qingxia Liu, Gong Cheng, Kalpa Gunaratna, Yuzhong Qu. [ESBM: An Entity Summarization BenchMark](https://arxiv.org/abs/2003.03734v1). arXiv:2003.03734v1, ESWC 2020.
1. Qingxia Liu, Gong Cheng, Yuzhong Qu. [DeepLENS: Deep Learning for Entity Summarization](https://arxiv.org/abs/2003.03736v1). arXiv:2003.03736v1, DL4KG 2020.
1. Junyou Li, Gong Cheng, Qingxia Liu, Wen Zhang, Evgeny Kharlamov, Kalpa Gunaratna, Huajun Chen. [Neural Entity Summarization with Joint Encoding and Weak Supervision](https://arxiv.org/abs/2005.00152v2). arXiv:2005.00152v2, IJCAI-PRICAI 2020.
1. Dongjun Wei, Yaxin Liu, Fuqing Zhu, Liangjun Zang, Wei Zhou, Yijun Lu, Songlin Hu. [AutoSUM: Automating Feature Extraction and Multi-user Preference Simulation for Entity Summarization](https://arxiv.org/abs/2005.11888v1). arXiv:2005.11888v1, PAKDD 2020.


### Evaluation Metrics

1. Chin-Yew Lin and Eduard Hovy. [Automatic Evaluation of Summaries Using N-gram
Co-Occurrence Statistics](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/naacl2003.pdf). In Proceedings of the Human Technology Conference 2003 (HLT-NAACL-2003).
2. Chin-Yew Lin. [Rouge: A package for automatic evaluation of summaries](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/was2004.pdf). Workshop on Text Summarization Branches Out, Post-Conference Workshop of ACL 2004.
3. Kishore Papineni, Salim Roukos, Todd Ward, and Wei-Jing Zhu. [BLEU: a Method for Automatic Evaluation of Machine Translation](http://www.aclweb.org/anthology/P02-1040.pdf).
4. Arman Cohan, Nazli Goharian. [Revisiting Summarization Evaluation for Scientific Articles](https://arxiv.org/abs/1604.00400v1). arXiv:1604.00400, LREC, 2016.
5. Maxime Peyrard. [A Simple Theoretical Model of Importance for Summarization](https://arxiv.org/abs/1801.08991v2). arXiv:1801.08991v2, ACL19 (outstanding paper award), 2019.
6. Kavita Ganesan. [ROUGE 2.0: Updated and Improved Measures for Evaluation of Summarization Tasks](https://arxiv.org/abs/1803.01937v1). arXiv:1803.01937, 2018. It works by comparing an automatically produced summary or translation against a set of reference summaries (typically human-produced).  ROUGE is one of the standard ways to compute effectiveness of auto generated summaries. The evaluation toolkit [ROUGE 2.0](https://github.com/RxNLP/ROUGE-2.0) is an easy to use  for Automatic Summarization tasks. 
7. Hardy, Shashi Narayan, Andreas Vlachos. [HighRES: Highlight-based Reference-less Evaluation of Summarization](https://arxiv.org/abs/1906.01361v1). arXiv:1906.01361v1, ACL 2019.
7. Wojciech Kryściński, Nitish Shirish Keskar, Bryan McCann, Caiming Xiong, Richard Socher. [Neural Text Summarization: A Critical Evaluation](https://arxiv.org/abs/1908.08960v1). arXiv:1908.08960v1, 2019.
1. Yuning Mao, Liyuan Liu, Qi Zhu, Xiang Ren, Jiawei Han. [Facet-Aware Evaluation for Extractive Summarization](https://arxiv.org/abs/1908.10383v2). arXiv:1908.10383v2, ACL 2020. Data can be found at [FAR](https://github.com/morningmoni/FAR).
7. Thomas Scialom, Sylvain Lamprier, Benjamin Piwowarski, Jacopo Staiano. [Answers Unite! Unsupervised Metrics for Reinforced Summarization Models](https://arxiv.org/abs/1909.01610v1). arXiv:1909.01610v1, 2019.
1. Erion Çano, Ondřej Bojar. [Efficiency Metrics for Data-Driven Models: A Text Summarization Case Study](https://arxiv.org/abs/1909.06618v1). arXiv:1909.06618v1, 2019.
1. Wojciech Kryściński, Bryan McCann, Caiming Xiong, Richard Socher. [Evaluating the Factual Consistency of Abstractive Text Summarization](https://arxiv.org/abs/1910.12840). arXiv:1910.12840v1, 2019.
1. Joshua Maynez, Shashi Narayan, Bernd Bohnet, Ryan McDonald. [On Faithfulness and Factuality in Abstractive Summarization](https://arxiv.org/abs/2005.00661v1). arXiv:2005.00661v1, ACL 2020.
1. Rahul Jha, Keping Bi, Yang Li, Mahdi Pakdaman, Asli Celikyilmaz, Ivan Zhiboedov, Kieran McDonald. [Artemis: A Novel Annotation Methodology for Indicative Single Document Summarization](https://arxiv.org/abs/2005.02146v2). arXiv:2005.02146v2, 2020.
1. Yang Gao, Wei Zhao, Steffen Eger. [SUPERT: Towards New Frontiers in Unsupervised Evaluation Metrics for Multi-Document Summarization](https://arxiv.org/abs/2005.03724v1). arXiv:2005.03724v1, ACL 2020. All source code is available at [acl20-ref-free-eval](https://github.com/yg211/acl20-ref-free-eval).
1. Esin Durmus, He He, Mona Diab. [FEQA: A Question Answering Evaluation Framework for Faithfulness Assessment in Abstractive Summarization](https://arxiv.org/abs/2005.03754v1). arXiv:2005.03754v1, ACL 2020.
1. Forrest Sheng Bao, Hebi Li, Ge Luo, Cen Chen, Yinfei Yang, Minghui Qiu. [End-to-end Semantics-based Summary Quality Assessment for Single-document Summarization](https://arxiv.org/abs/2005.06377v1). arXiv:2005.06377v1, 2020.
1. Daniel Deutsch, Dan Roth. [SacreROUGE: An Open-Source Library for Using and Developing Summarization Evaluation Metrics](https://arxiv.org/abs/2007.05374v1). arXiv:2007.05374v1, 2020.
1. Alexander R. Fabbri, Wojciech Kryściński, Bryan McCann, Caiming Xiong, Richard Socher, Dragomir Radev. [SummEval: Re-evaluating Summarization Evaluation](https://arxiv.org/abs/2007.12626v3). arXiv:2007.12626v3, 2020. The source code is available [SummEval](https://github.com/Yale-LILY/SummEval).


### Opinion Summarization

1. Kavita Ganesan, ChengXiang Zhai and Jiawei Han. [Opinosis: A Graph Based Approach to Abstractive Summarization of Highly Redundant Opinions](http://kavita-ganesan.com/opinosis). Proceedings of COLING '10, 2010.
2. Kavita Ganesan, ChengXiang Zhai and Evelyne Viegas. [Micropinion Generation: An Unsupervised Approach to Generating Ultra-Concise Summaries of Opinions](http://kavita-ganesan.com/micropinion-generation). WWW'12, 2012.
3. Kavita Ganesan. [Opinion Driven Decision Support System (ODSS)](http://kavita-ganesan.com/phd-thesis). PhD Thesis, University of Illinois at Urbana-Champaign, 2013.
4. Ozan Irsoy and Claire Cardie. [Opinion Mining with Deep Recurrent Neural Networks](https://www.cs.cornell.edu/~oirsoy/files/emnlp14drnt.pdf). In EMNLP, 2014.
5. Ahmad Kamal. [Review Mining for Feature Based Opinion Summarization and Visualization](https://arxiv.org/abs/1504.03068v2). arXiv:1504.03068, 2015.
6. Haibing Wu, Yiwei Gu, Shangdi Sun and Xiaodong Gu. [Aspect-based Opinion Summarization with Convolutional Neural Networks](https://arxiv.org/abs/1511.09128). 2015.
7. Lu Wang, Hema Raghavan, Claire Cardie, Vittorio Castelli. [Query-Focused Opinion Summarization for User-Generated Content](https://arxiv.org/abs/1606.05702v1). arXiv:1606.05702, 2016.
8. Reinald Kim Amplayo, Mirella Lapata. [Informative and Controllable Opinion Summarization](https://arxiv.org/abs/1909.02322v1). arXiv:1909.02322v1, 2019.
1. Arthur Bražinskas, Mirella Lapata, Ivan Titov. [Unsupervised Multi-Document Opinion Summarization as Copycat-Review Generation](https://arxiv.org/abs/1911.02247v1). arXiv:1911.02247v1, 2019.
1. Tianjun Hou (LGI), Bernard Yannou (LGI), Yann Leroy, Emilie Poirson (IRCCyN). [Mining customer product reviews for product development: A summarization process](https://arxiv.org/abs/2001.04200v1). arXiv:2001.04200v1, 2020. 
1. Reinald Kim Amplayo, Mirella Lapata. [Unsupervised Opinion Summarization with Noising and Denoising](https://arxiv.org/abs/2004.10150v1). arXiv:2004.10150v1, ACL 2020.
1. Hady Elsahar, Maximin Coavoux, Matthias Gallé, Jos Rozen. [Self-Supervised and Controlled Multi-Document Opinion Summarization](https://arxiv.org/abs/2004.14754v2). arXiv:2004.14754v2, 2020.
1. Arthur Bražinskas, Mirella Lapata, Ivan Titov. [Few-Shot Learning for Abstractive Multi-Document Opinion Summarization](https://arxiv.org/abs/2004.14884v1). arXiv:2004.14884v1, 2020.
1. Yoshihiko Suhara, Xiaolan Wang, Stefanos Angelidis, Wang-Chiew Tan. [OpinionDigest: A Simple Framework for Opinion Summarization](https://arxiv.org/abs/2005.01901v1). arXiv:2005.01901v1, ACL 2020.
1. Nofar Carmeli, Xiaolan Wang, Yoshihiko Suhara, Stefanos Angelidis, Yuliang Li, Jinfeng Li, Wang-Chiew Tan. [ExplainIt: Explainable Review Summarization with Opinion Causality Graphs](https://arxiv.org/abs/2006.00119v1). arXiv:2006.00119v1, 2020.
1. Pengyuan Li, Lei Huang, Guang-jie Ren. [Topic Detection and Summarization of User Reviews](https://arxiv.org/abs/2006.00148v1). arXiv:2006.00148v1, 2020.
1. Rajdeep Mukherjee, Hari Chandana Peruri, Uppada Vishnu, Pawan Goyal, Sourangshu Bhattacharya, Niloy Ganguly. [Read what you need: Controllable Aspect-based Opinion Summarization of Tourist Reviews](https://arxiv.org/abs/2006.04660v2). arXiv:2006.04660v2, 2020.
