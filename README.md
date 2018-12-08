# RadiologyReportEmbedding

Paper in AMIA 2017: Banerjee, Imon, Sriraman Madhavan, Roger Eric Goldman, and Daniel L. Rubin. "Intelligent Word Embeddings of Free-Text Radiology Reports." In AMIA Annual Symposium Proceedings, vol. 2017, p. 411. American Medical Informatics Association, 2017.
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5977573/

A hybrid strategy that combines semantic-dictionary mapping and word2vec modeling, has been applied to create the word embeddings from ~10,000 CT Head radiology reports.  

We followed the following step: Data set retrieval from PACS, Data Cleaning & Pre-processing, Semantic-dictionary mapping (CLEVER and RadLex terminology), and Word and Report Embedding via Continuous Bag Of Word model. The size of the resulting vocabulary was 4,442 words.

Using the vector representation, we automatically classify them into three classes denoting the confidence in the diagnosis of intracranial hemorrhage by the interpreting radiologist. We performed a range of experiments with different classifiers and varying hyper-parameters settings. Best performance achieved is weighted precision of 88% and weighted recall of 90%. 

The Radiology word vectors can be resued in similar classification scenarios or can be used to interpret word-to-word relations.


Using a prebuilt model:

1. Get python 2.7

2. unzip modelname.zip -d destination_folderpath

3. Install gensim: pip install gensim


4. Load model in gensim:

  from gensim.models import Word2Vec

  model = Word2Vec.load(modelpath)

  model.similarity('new', 'recent') %used to find the cosine distance

