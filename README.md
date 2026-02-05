# Molecular-Property-Prediction-using-GNNs-GCN-vs-GINE-on-FreeSolv-dataset-PyTorch-Geometric

This project explores the use of Graph Neural Networks (GNNs) for predicting molecular properties from SMILES representations.  
Two architectures are implemented and compared:

- Graph Convolutional Network (GCN)
- Graph Isomorphism Network with Edge Features (GINE)


## Project Overview

Molecules naturally form graph structures where:

- Atoms → Nodes  
- Bonds → Edges  

Traditional neural networks cannot directly process such relational data.  
Graph Neural Networks are designed specifically to operate on this type of structured information.


## Models Implemented

### 1. Graph Convolutional Network (GCN)

**Key Idea**

- Each node updates its representation by aggregating information from neighbouring nodes.
- Uses adjacency matrix and mean aggregation.
- Does not explicitly use edge features.



### 2. Graph Isomorphism Network with Edge Features (GINE)

**Why GINE?**

- Designed to handle both node and edge features  
- More expressive than standard GCN  
- Better suited for molecular graphs

**Working Principle**
For each node:

1. Collect neighbouring node features  
2. Collect corresponding edge (bond) features  
3. Combine them  
4. Pass through an MLP  
5. Aggregate using sum aggregation  
6. Update node representation



## Dataset Description

The FreeSolv dataset is a curated collection of experimental and computed hydration free energies for small organic molecules in water. It is widely used as a benchmark dataset for molecular machine learning and regression tasks.
* Task type: Regression (predict continuous hydration free energy) 
* Dataset size: ~642 small neutral molecules 
* Molecular representation:
    * SMILES strings describing structure
    * Graph representation with node features (atom attributes) and edge features (bond information) 
* Target property: Experimental hydration free energy (in kcal/mol), representing how favourable it is for a molecule to dissolve in water. 
FreeSolv was originally compiled with experimental measurements drawn from literature and supplemented with calculated hydration values using molecular dynamics approaches. Its original publication describes 643 small molecules along with hydration free energy values.



## Technologies Used

- Python  
- PyTorch  
- PyTorch Geometric  
- RDKit  
- NumPy, Pandas  
- Matplotlib, Seaborn


## NOTE : RESULTS MAY CHANGE SLIGHTLY BECAUSE OF THE SHUFFLING IN DATASET , RANDOMISED WEIGHTS BY PYTORCH. I HAVE MENTIONED THE RESULTS BASED ON MY FINAL TRAINING 





HAVE A FUN TIME LEARNING ;)

-HSB(Author)
