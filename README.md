# Vegetables 

This is a collection of word embeddings repackaged for easy machine loading and human reading. 

Each set of embeddings should come with the following files:
 
 - `.tsv` is a tab separated file where the 
   - (i) first column is the word/token, 
   - (ii) second column is the count (if the original pre-trained embedding didn't save any count, it will be set to -1), 
   - (iii) the third to the last columns form the actual embedding for the word/token in the first column.
 - `.txt` is the key words
   - same as the first column in the `.tsv` file.
 - `.npy` is the word embedding that can be directly loaded with `numpy`
   - same as the third to last columns in the `.tsv` file.
 - `.pkl` is a pickled file with its keys as the word/token and the count of the word/token.
   - if the original pre-trained embedding didn't save any count, it will be set to -1
 
 
Usage
====

```python
>>> import pickle 
>>> import numpy as np

>>> embeddings = np.load('hlbl.rcv1.original.50d.npy')
>>> tokens = [line.strip() for line in open('hlbl.rcv1.original.50d.txt')]
>>> embeddings[tokens.index('hello')]
array([-0.21167406, -0.04189226,  0.22745571, -0.09330438,  0.13239339,
        0.25136262, -0.01908735, -0.02557277,  0.0029353 , -0.06194451,
       -0.22384156,  0.04584747,  0.03227248, -0.13708033,  0.17901117,
       -0.01664691,  0.09400477,  0.06688628, -0.09019949, -0.06918809,
        0.08437972, -0.01485273, -0.12062263,  0.05024147, -0.00416972,
        0.04466985, -0.05316647,  0.00998635, -0.03696947,  0.10502578,
       -0.00190554,  0.03435732, -0.05715087, -0.06777468, -0.11803425,
        0.17845355,  0.18688948, -0.07509124, -0.16089943,  0.0396672 ,
       -0.05162677, -0.12486628, -0.03870481,  0.0928738 ,  0.06197058,
       -0.14603543,  0.04026282,  0.14052328,  0.1085517 , -0.15121481])
```


Monolingual 
=====

| Pre-trained Embeddings | Type | Lang | Cite | Year | Bib | License | Kaggle Dataset |
|:-|:-:|:-:|:-|:-:|:-:|:-:|:-|
| [Senna](https://ronan.collobert.com/senna/) (aka. C&W) | LM2 | eng | [Collobert et al.](http://www.jmlr.org/papers/volume12/collobert11a/collobert11a.pdf) (aka. C&W) | 2008/2011 | [bib](https://dl.acm.org/downformats.cfm?id=1390177&parent_id=1390156&expformat=bibtex)/<br>[bib](https://dl.acm.org/downformats.cfm?id=2078186&parent_id=1953048&expformat=bibtex) | [![License](https://img.shields.io/badge/License-Others-red.svg)](https://ronan.collobert.com/senna/download.html) | [senna-embeddings](https://www.kaggle.com/alvations/vegetables-senna-embeddings) |
| [Turian Embeddings](https://www.kaggle.com/alvations/turian-embeddings) (aka. HLBL)|  Brown, C&W, HLBL | eng | [Turian et al.](http://anthology.aclweb.org/P/P10/P10-1040.pdf) | 2011 | [bib](https://aclanthology.info/papers/P10-1040/p10-1040.bib)| [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | [hlbl-embeddings](https://www.kaggle.com/alvations/vegetables-hlbl-embeddings) | 
| [Huang Embeddings](https://www.kaggle.com/alvations/huang-embeddings) (aka. Huang)| Huang | eng | [Huang et al.](http://www.aclweb.org/anthology/P12-1092) | 2012 | [bib](https://aclanthology.info/papers/P12-1092/p12-1092.bib)| [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | ! [huang-embeddings](https://www.kaggle.com/alvations/vegetables-huang-embeddings) | 
| [Word2Vec (News)](https://code.google.com/archive/p/word2vec/) | word2vec | eng |  [Mikolov et al.](https://arxiv.org/abs/1301.3781) | 2013 | [bib](https://dblp.uni-trier.de/rec/bibtex/journals/corr/abs-1301-3781) | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [google-word2vec](https://www.kaggle.com/alvations/vegetables-google-word2vec) 
| [Word2Vec (Freebase)](https://code.google.com/archive/p/word2vec/) | word2vec | eng | [Mikolov et al.](https://arxiv.org/abs/1301.3781) | 2013| [bib](https://dblp.uni-trier.de/rec/bibtex/journals/corr/abs-1301-3781) | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [google-word2vec-freebase](https://www.kaggle.com/alvations/vegetables-google-word2vec-freebase) |
| [morphoRNN](https://nlp.stanford.edu/~lmthang/morphoNLM/) | Huang, C&W | eng | [Luong et al.](http://www.aclweb.org/anthology/W13-3512) | 2013 | [bib](https://aclanthology.info/papers/W13-3512/w13-3512.bib) | [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | [csrnn-embeddings](https://www.kaggle.com/alvations/vegetables-csrnn-embeddings) | 
| [GloVe (6B)](https://nlp.stanford.edu/projects/glove/)      |GloVe| eng | [Pennington et al.](https://www.aclweb.org/anthology/D14-1162) | 2014 | [bib](https://aclanthology.info/papers/D14-1162/d14-1162.bib) | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [stanford-glove-6b](https://www.kaggle.com/alvations/vegetables-stanford-glove-6b)|
| [GloVe (42B)](https://nlp.stanford.edu/projects/glove/)     |GloVe| eng | [Pennington et al.](https://www.aclweb.org/anthology/D14-1162) | 2014 |[bib](https://aclanthology.info/papers/D14-1162/d14-1162.bib) | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [stanford-glove-42b](https://www.kaggle.com/alvations/vegetables-stanford-glove-42b)|
| [GloVe (840B)](https://nlp.stanford.edu/projects/glove/)    |GloVe| eng |[Pennington et al.](https://www.aclweb.org/anthology/D14-1162) | 2014 |[bib](https://aclanthology.info/papers/D14-1162/d14-1162.bib) | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [stanford-glove-840b](https://www.kaggle.com/alvations/vegetables-stanford-glove-840b)|
| [GloVe (Twitter)](https://nlp.stanford.edu/projects/glove/) |GloVe| eng | [Pennington et al.](https://www.aclweb.org/anthology/D14-1162) | 2014 | [bib](https://aclanthology.info/papers/D14-1162/d14-1162.bib) | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [stanford-glove-twitter](https://www.kaggle.com/alvations/vegetables-stanford-glove-twitter)|
| [COMPOSES](http://clic.cimec.unitn.it/composes/semantic-vectors.html)        | word2vec | eng | [Baroni et al.](http://www.aclweb.org/anthology/P14-1023) | 2014 | [bib](https://aclanthology.info/papers/P14-1023/p14-1023.bib) | [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/80x15.png)](https://creativecommons.org/licenses/by/4.0/) | [composes-embeddings](https://www.kaggle.com/alvations/vegetables-composes-embeddings) |
| [Dependency](https://levyomer.wordpress.com/2014/04/25/dependency-based-word-embeddings/) | word2vec | eng | [Levy and Golberg](http://www.aclweb.org/anthology/P14-2050) | 2014 | [bib](https://aclanthology.info/papers/P14-2050/p14-2050.bib) | [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | [dependency-embeddings](https://www.kaggle.com/alvations/vegetables-dependency-embeddings)|
| [Word2Vec (Shiroyagi)](https://github.com/shiroyagicorp/japanese-word2vec-model-builder) | word2vec | jap | [Shiroyagi Corp.](http://aial.shiroyagi.co.jp/2017/02/japanese-word2vec-model-builder/) | 2017 | ~ | [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) | [shiroyagi-word2vec](https://www.kaggle.com/alvations/vegetables-shiroyagi-word2vec) | 

<!-- 

| [ECO](https://github.com/azpoliak/eco)   | skip-embeds | eng | [Adam et al.](http://www.aclweb.org/anthology/E17-2081) | 2017 | | [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | ! [eco-embeddings]() | 



Multilingual
=====

| Pre-trained Embeddings | Type | #Langs | Langs | Cite | Year | Bib | License |  Kaggle Dataset |
|:-|:-:|:-:|:-:|:-:|:-:|:-:|:-|:-|
| [Polyglot](https://sites.google.com/site/rmyeid/projects/polyglot) | Senna | 117 | ... | [Al-Rfou et al.](http://www.google.com/url?q=http%3A%2F%2Fwww.aclweb.org%2Fanthology%2FW13-3520&sa=D&sntz=1&usg=AFQjCNHFu1aPKusZX5amgWa_RrOP9cbh6w) | 2013 | [bib]() | | |
| [HistWords](https://nlp.stanford.edu/projects/histwords/)        | word2vec |  4 | cmn,deu,eng,fre | [Hamilton et al.](https://aclweb.org/anthology/P/P16/P16-1141.pdf) | 2016 | [bib]() | [![License: ODbL](https://img.shields.io/badge/License-PDDL-brightgreen.svg)](https://opendatacommons.org/licenses/pddl/) | ! [histwords-embeddings]() | 
| [Fasttext](https://fasttext.cc/) | fasttext | 157 | ... | [Grave et al.](http://www.lrec-conf.org/proceedings/lrec2018/pdf/627.pdf) | 2018 | [bib]() | [![License: CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/) | ! [fasttext-embeddings]() | 


-->
