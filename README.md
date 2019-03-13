# ACE-Drug
## Advanced Computational Engine (ACE) for Drug Discovery

This repository introduces codes on **"deep neural network based screening models for drug discovery", coined ACE-Drug**. 
We evaluated our model performances with various studies on graph convolutional network, its augmentations, regularizations, normalization techniques. 

We tested ACE-Drug on the following datasets:
* **Large** (Datasets consisting of more than 10k number of molecules) : ZINC, HIV, CEP
* **Small** (Datasets consisting of less than 10k number of molecules) : BBBP, BACE, ClinTox, ESOL, FreeSolv, Lipophilicity
* **Multi-task** (Datasets whose sample molecules have multiple molecular properties) : Tox21, SIDER

For the utilization of our models with a few data, we provide following methods:
* **Bayesian inference** : In contrast to ML/MAP estimations of model parameters, it is able to estimate uncertainties in our predictions with Bayeisan inference. We implemented a MC-dropout sampling method to quantify uncertainties. 
* **Transfer learning** : 

In what follows, we executed follwing experiments

### Exp.1 : Augmentation of graph convolutional network
In this experiment, we show the effect of attention and gated mechanisms to augment the graph convolutional networks. 
In order to observe the effect of augmentations, we trained the models with "Large" dataset.
* Accuracy of models with respect to the number of graph convolution layers.
* Accuracy of models on the prediction of logP, TPSA, SAS, PCE and HIV-activity. 

### Exp.2 : Effect of the normalization techniques
Normalization techniques, i.e. batch/layer/instance/weight/... normalizations, have been widely adopted in deep neural networks to accerelate training process. However, to the best of our knowledge, we could not find studies on the effect of normalizations to graph neural network. 
To elucidate it, we show the 


