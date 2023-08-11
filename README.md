# Liar_Detection_Project

#### The publication related to this project can be found in this [link](https://ieeexplore.ieee.org/document/10195000).

In this project, I explored various methodologies to identify the optimal approach for distinguishing between fake and genuine news articles. These methodologies includes a spectrum of data cleansing techniques, distinct classification approaches, and varied methods for modeling and visualization. The experiments in this project fall into two categories. The first category is done using binary classification and downsampling the data into a balanced dataset, capturing the Fake and Real statements. The second category consists of three classes of False, True and Lie statements. These experiments are done within different Notebooks.  

## How:
To begin with, I employed the LIAR dataset, [accessible here](https://arxiv.org/abs/1705.00648), to investigate the issue and delve into the specifics of the available dataset. 
<br />
In the next step, I cleaned and prepared the data for vectorizing using various methods like 
Upon evaluating various machine learning models, I concluded my project by selecting three distinct models:
1. BERT model: The pre-trained model called "bert-base-uncased" from the Huggingface open-source library is used to vectorize the statements of LIAR dataset. 
2. Doc2vecc algorithm: To transform the statements column of the statements in the LIAR dataset I implemented Doc2vecC model inspired from this [paper](https://arxiv.org/abs/1707.02377). Then created the "docvectors.txt" consists of 256 feature vectors for each statement.
3. SBert model: SBERT embeds sentences faster and more accurately in comparison to BERT and its optimized variant, RoBERTa.
<br />
After implementing the models, I applied KNN and SVM to classify the embeddings I captured above.

## Results:
The evaluation results can be found in the TABLE I, accessible [here](https://ieeexplore.ieee.org/document/10195000)
<br />
| models      | Accuracy    | Training Accuracy |   Kappa Score |  F-1  |  Precision  |  Recall  |  ROC Accuracy  | 
| :---        |    :----:   |        :---:      |     :---:     | :---: |    :---:    |   :---:  |    ---:        |
| BERT+SVM    | 36.87%      | 47.82%            |  05.31%       | 51.96%|    60.26%   |  47.82%  |  56.24%        |
| BERT+KNN    | 32.56%      | 55.71%            |  33.57%       | 37.65%|    60.15%   |  32.56%  |  53.32%        |
| BERT+SVM    | 30.27%      | 68.10%            |  52.15%       | 33.17%|    56.40%   |  30.27%  |  45.38%        |
| BERT+KNN    | 44.66%      | 55.47%            |  33.21%       | 48.37%|    53.31%   |  44.66%  |  44.63%        |
| BERT+SVM    | 45.61%      | 89.40%            |  84.10%       | 51.17%|    65.87%   |  45.61%  |  63.43%        |
| BERT+KNN    | 39.13%      | 60.65%            |  40.97%       | 45.01%|    63.87%   |  39.13%  |  59.70%        |

## Get familiar with files in this project:
1. Binary classification and multiclass classification folder: consists of Notebooks related to the final results.
2. alldata.vocab: The dictionary of vocabulary that the doc2vecc created from the statements.
3. doc2vecc: Compiled file of doc2vecc.c
4. doc2vecc.c: The original algorithm in "C".
5. docvectors.txt: Vectors created by doc2vecc algorithm of all statements.
6. go.sh: The script that is applying the algorithm to all data that is provided in statements folder.
7. train.tsv: Original source of data.
8. wordvectors.txt: Vectors created for each vocabulary in the alldata.vocab file.
9. statements: This folder contains all the statement rows from the preprocessed data as a txt file.
10. bash foler: consists of files related to the doc2vecC embeddings and shell scripting.
11. statements folder: consists of statement text files.
