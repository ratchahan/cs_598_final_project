# CS 598 Final Project - SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS
Final Project for CS 598 Deep Learning for Healthcare

>📋  A template README.md for code accompanying a Machine Learning paper

# SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS

This repository is the official implementation of [SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS](https://arxiv.org/abs/1609.02907). 

>📋  Our code submission is in the form of a jupyter notebook. This was approved in Campuswire post #1957

## Requirements

All additional requirements are installed in the notebook:

```setup
!pip install dgl
```


## Training and Evaluation

To train and evaluate the model(s) in the paper with the three citation network datasets, run one of these three commands (note this is included in a cell in the notebook):

```train
citeseer_dataset =  dgl.data.CiteseerGraphDataset()
train_and_test_model(citeseer_dataset)
```

```train
cora_dataset =  dgl.data.CoraGraphDataset()
train_and_test_model(cora_dataset)
```

```train
pubmed_dataset =  dgl.data.PubmedGraphDataset()
train_and_test_model(pubmed_dataset)
```


## Results

Our model achieves the following performance with the three citation networks from the paper:


| Model                | Citeseer    | Cora       | Pubmed     |
|----------------------|-------------|------------|------------|
| GCN (original paper) | 70.3 (7s)   | 81.5 (4s)  | 79.0 (38s) |
| GCN (Pytorch)        | 70.5 (2.35s)| 81.6 (0.96s)| 78.5 (1.16s)|

Note that there are additional ablations we implemented (Renormalization Removal and Sparse Matrix Multiplication Removal). The results for these ablation studies are documented in the notebook. 


