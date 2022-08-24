# Liar_Detection_Project

In this project I tried to find the latent features of the Liar dataset that is available publicly.

## How?
I applied the "doc2vecc" algrithm to transform the statements column of the "train.tsv" file and created the "docvectors.txt" consists of 256 feature vectors for each statement.

## Results?
So far the results of this project is accessible via "Liar_Detection.ipynb" file. I'm still working on this project to find the best way to find the latent features of this dataset.

## Get familiar with files in this project:
1. Liar_Detection.ipynb: The Jupyter notebook I'm currently working on to find meaningful latent features. This Notebook consists of cleaning data, implementing and applying doc2vecc algorithm, applying KNN, TSNE and PCA on the transformed data, and implemented Bert model.
2. alldata.vocab: The dictionary of vocabulary that the doc2vecc created from the statements.
3. doc2vecc: Compiled file of doc2vecc.c
4. doc2vecc.c: The original algorithm in "C".
5. docvectors.txt: Vectors created by doc2vecc algorithm of all statements.
6. go.sh: The script that is applying the algorithm to all data that is provided in statements folder.
7. train.tsv: Original source of data.
8. wordvectors.txt: Vectors created for each vocabulary in the alldata.vocab file.
9. statements: This folder contains all the statement rows from the preprocessed data as a txt file.
