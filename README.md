# Vegetables 

This is a collection of word embeddings repackaged for easy machine loading and human reading. 

Each set of embeddings should come with the following files:
 
 - `.tsv` is a tab separated file where the 
   - (i) first column is the word/token, 
   - (ii) second column is the count (if the original pre-trained embedding didn't save any count, it will be set to -1), 
   - (iii) the third to the last columns form the actual embedding for the word/token in the first column.
 - `.txt` is the key words; same as the first column in the `.tsv` file.
 - `.npy` is the word embedding that can be directly loaded with `numpy`; same as the third to last columns in the `.tsv` file.
 - `.pkl` is a pickled file with its keys as the word/token and the value is the embeddings as a `list(float)` type.
 
 
Usage
====

```
import pickle 
import numpy as np


```


Monolingual 
=====

| Pre-trained Embeddings | Type | Lang | Cite | Year | Bib | License | Kaggle Dataset |
|:-|:-:|:-:|:-|:-:|:-:|:-:|:-|
| [Senna](https://ronan.collobert.com/senna/)           | LM2 | eng | [Collobert et al.](http://www.jmlr.org/papers/volume12/collobert11a/collobert11a.pdf) | 2011 |  | [![License](https://img.shields.io/badge/License-Others-red.svg)](https://ronan.collobert.com/senna/download.html) | [senna-embeddings](https://www.kaggle.com/alvations/vegetables-senna-embeddings) |
| [Turian Embeddings](https://www.kaggle.com/alvations/turian-embeddings) |  Brown, C&W, HLBL | eng | [Turian et al.](http://anthology.aclweb.org/P/P10/P10-1040.pdf) | 2011 | | [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | [hlbl-embeddings](https://www.kaggle.com/alvations/vegetables-hlbl-embeddings) | 
| [Word2Vec (News)](https://code.google.com/archive/p/word2vec/) | word2vec | eng |  [Mikolov et al.](https://arxiv.org/abs/1301.3781) | 2013 | | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [google-word2vec](https://www.kaggle.com/alvations/vegetables-google-word2vec) 
| [Word2Vec (Freebase)](https://code.google.com/archive/p/word2vec/) | word2vec | eng | [Mikolov et al.](https://arxiv.org/abs/1301.3781) | 2013| | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [google-word2vec-freebase](https://www.kaggle.com/alvations/vegetables-google-word2vec-freebase) |
| [morphoRNN](https://nlp.stanford.edu/~lmthang/morphoNLM/) | word2veec | eng | [Luong et al.](http://www.aclweb.org/anthology/W13-3512) | 2013 | | [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | | 
| [GloVe (6B)](https://nlp.stanford.edu/projects/glove/)      |GloVe| eng | [Pennington et al.](https://www.aclweb.org/anthology/D14-1162) | 2014 | | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [stanford-glove-6b](https://www.kaggle.com/alvations/vegetables-stanford-glove-6b)|
| [GloVe (42B)](https://nlp.stanford.edu/projects/glove/)     |GloVe| eng | [Pennington et al.](https://www.aclweb.org/anthology/D14-1162) | 2014 | | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [stanford-glove-42b](https://www.kaggle.com/alvations/vegetables-stanford-glove-42b)|
| [GloVe (840B)](https://nlp.stanford.edu/projects/glove/)    |GloVe| eng |[Pennington et al.](https://www.aclweb.org/anthology/D14-1162) | 2014 | | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [stanford-glove-840b](https://www.kaggle.com/alvations/vegetables-stanford-glove-840b)|
| [GloVe (Twitter)](https://nlp.stanford.edu/projects/glove/) |GloVe| eng | [Pennington et al.](https://www.aclweb.org/anthology/D14-1162) | 2014 | | [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) | [stanford-glove-twitter](https://www.kaggle.com/alvations/vegetables-stanford-glove-twitter)|
| [COMPOSES](http://clic.cimec.unitn.it/composes/semantic-vectors.html)        | word2vec | eng | [Baroni et al.](http://www.aclweb.org/anthology/P14-1023) | 2014 | [bib]() | [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/80x15.png)](https://creativecommons.org/licenses/by/4.0/) | [composes-embeddings](https://www.kaggle.com/alvations/vegetables-composes-embeddings) |
| [Dependency](https://levyomer.wordpress.com/2014/04/25/dependency-based-word-embeddings/) | word2vec | eng | [Levy and Golberg](http://www.aclweb.org/anthology/P14-2050) | 2014 | | [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | [dependency-embeddings](https://www.kaggle.com/alvations/vegetables-dependency-embeddings)|
| [Word2Vec (Shiroyagi)](https://github.com/shiroyagicorp/japanese-word2vec-model-builder) | word2vec | jap | [Shiroyagi Corp.](http://aial.shiroyagi.co.jp/2017/02/japanese-word2vec-model-builder/) | 2017 |  | [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) | [shiroyagi-word2vec](https://www.kaggle.com/alvations/vegetables-shiroyagi-word2vec) | 
| [ECO](https://github.com/azpoliak/eco)   | skip-embeds | eng | [Adam et al.](http://www.aclweb.org/anthology/E17-2081) | 2017 | | [![License](https://img.shields.io/badge/License-Unknown-ff69b4.svg)]() | ! [eco-embeddings]() | 


Multilingual
=====

| Pre-trained Embeddings | Type | #Langs | Langs | Cite | Year | Bib | License |  Kaggle Dataset |
|:-|:-:|:-:|:-:|:-:|:-:|:-:|:-|:-|
| [Polyglot](https://sites.google.com/site/rmyeid/projects/polyglot) | Senna | 117 | ... | [Al-Rfou et al.](http://www.google.com/url?q=http%3A%2F%2Fwww.aclweb.org%2Fanthology%2FW13-3520&sa=D&sntz=1&usg=AFQjCNHFu1aPKusZX5amgWa_RrOP9cbh6w) | 2013 | [bib]() | | |
| [HistWords](https://nlp.stanford.edu/projects/histwords/)        | word2vec |  4 | cmn,deu,eng,fre | [Hamilton et al.](https://aclweb.org/anthology/P/P16/P16-1141.pdf) | 2016 | [bib]() | [![License: ODbL](https://img.shields.io/badge/License-PDDL-brightgreen.svg)](https://opendatacommons.org/licenses/pddl/) | ! [histwords-embeddings]() | 
| [Fasttext](https://fasttext.cc/) | fasttext | 157 | ... | [Grave et al.](http://www.lrec-conf.org/proceedings/lrec2018/pdf/627.pdf) | 2018 | [bib]() | [![License: CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/) | ! [fasttext-embeddings]() | 

