# AML4DS2024_Julius_and_Sebastian
The code and README for Julius and Sebastian's mini-project for AML4DS2024 - ComplEx mode on OBG's Biomedical Knowledge Graph (biokg) dataset.

***

THE DATASET: The biokg dataset consists of ~94K nodes and ~5,1M edges for five different entities: drugs, diseases, proteins, protein functions and side effects. In terms of KGs, it is a relatively "small" dataset, but the size and complexity of the dataset did prove to give us some trouble. We chose this dataset because one of the members in the group (Sebastian) works in a pharmaceutical company, and graphs have an impact on industry within the fields of drug safety and drug discovery. For instance, the antibiotic drug Halicin has in recent years been developed thanks to the use of GNNs in the early stages of drug discovery. 

GOALS: Our goal(s) were to 1) train a 'simple' Knowledge Graph Embedding (KGE) model on the biokg dataset as a baseline model, and 2) train and compare to a more advanced GNN, e.g. a GAT, to see evaluate the differences. We did not, unfortunately, manage to complete the second goal. The code includes our four attempts to train a model, visualizations of drug-drug triplets and a simple example from the dataset.

RESULTS: 

FINDINGS AND REFLECTIONS: Due to the more complex nature of the dataset (i.e. five different entities) and it being our first time working with graphs, we spent a large amount of time just understanding and navigating the dataset.  
