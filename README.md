# AML4DS2024_Julius_and_Sebastian
The code and README for Julius and Sebastian's mini-project for AML4DS2024 - ComplEx mode on OBG's Biomedical Knowledge Graph (biokg) dataset.

***

`THE DATASET` 
The biokg dataset consists of ~94K nodes and ~5,1M edges for five different entities: drugs, diseases, proteins, protein functions and side effects. In terms of KGs, it is a relatively "small" dataset, but the size and complexity of the dataset did prove to give us some trouble. We chose this dataset because one of the members in the group (Sebastian) works in a pharmaceutical company, and graphs have an impact on industry within the fields of drug safety and drug discovery. For instance, the antibiotic drug Halicin has in recent years been developed thanks to the use of GNNs in the early stages of drug discovery. 

`GOALS` 
Our goal(s) were to 1) train a 'simple' Knowledge Graph Embedding (KGE) model on the biokg dataset as a baseline model, and 2) train and compare to a more advanced GNN, e.g. a GAT, to see evaluate the differences. We did not, unfortunately, manage to complete the second goal. The code includes our four attempts to train a model, visualizations of drug-drug triplets and a simple example from the dataset.

`MODEL RUNs AND RESULTS` 
Due to its scale, we had to decrease the train, test and validation set to be able to train the ComplEx model during the first attempts. We have, therefore, created a smaller subset of the training data. This comes at the obvious cost of losing the underlying structure and logic of the KG, and our model can not be used to make link predictions.

We have utilsed the pytorch.geomtric library and imported an out-of-the-box version of the ComplEx model. For all model runs we utilised the Adam optimizer. 

| Attempt | Subset of training data | **Val MRR** | Hits@10 |
|---------|-------------------------|---------|---------|
| 1 |           10.000        |  0.007   | 0.012   |
| 2 |           10.000        | 0.4003    |0.6856*
| 3|    20.000              |0.0003 |   0.0003 |

The OGB leaderboard Val MRR score is 0.9627.

*It is important to note that we removed the L2 regularizer between attempt 1 and 2. The results are, therefore, likely due to overfitting.

In our code, we have also train two models based on a larger subset of the training data (35.000), but due to the limited time, we were not able to extend it to the entire dataset - and had to remove the validation set.  

`FINDINGS AND REFLECTIONS`
Due to the more complex nature of the dataset (i.e. five different entities) and it being our first time working with graphs, we spent a large amount of time just understanding and navigating the dataset. We couldn't train on the whole dataset and that likely meant that we lost the underlying logic of the data.  We have attempted other model runs than the ones above, where we managed to include more training data, and if time permitted, we are hopeful that we could have trained on the entire dataset.
