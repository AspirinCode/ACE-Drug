# ACE-Drug
## Advanced Computational Engine (ACE) for Drug Discovery

This repository introduces codes on **"deep neural network based screening models for drug discovery", coined ACE-Drug**. 
We evaluated our model performances with various studies on graph convolutional network, its augmentations, regularizations, normalization techniques. 

We tested ACE-Drug on the following datasets:
* **Large** (Datasets consisting of more than 10k number of molecules) : ZINC, HIV, CEP
* **Small** (Datasets consisting of less than 10k number of molecules) : BBBP, BACE, ClinTox, ESOL, FreeSolv, Lipophilicity
* **Multi-task** (Datasets whose sample molecules have multiple molecular properties) : Tox21, SIDER

For the utilization of our models with a few data, we provide the following methods:
* **Bayesian inference** : In contrast to ML/MAP estimations of model parameters, it is able to estimate uncertainties in our predictions with Bayeisan inference. We implemented a MC-dropout sampling method to quantify uncertainties. 
* **Transfer learning** : Transfer prior-knowledge can enhance the training of new tasks. To do so, we provide transfer learning methods with easy python scripts. 

In what follows, we executed follwing experiments

### Exp.1 : Augmentation of graph convolutional network
In this experiment, we show the effect of attention and gated mechanisms to augment the graph convolutional networks. 
In order to observe the effect of augmentations, we trained the models with "Large" dataset.
* Accuracy of models with respect to the number of graph convolution layers.
* Accuracy of models on the prediction of logP, TPSA, SAS, PCE and HIV-activity. 

### Exp.2 : Effect of normalization techniques
Normalization techniques, i.e. batch/layer/instance/weight/... normalizations, have been widely adopted in deep neural networks to accerelate training process. However, to the best of our knowledge, we could not find studies on the effect of normalizations to graph neural network. 

To elucidate it, we tested the effect of three normalization techniques, i.e. batch/layer/instance normalization.
* Change of model accuracy as the number of training epoch increases
* Model performances with respect to the three normalization techniques

### Exp.3 : Effect of regularization techniques
Deep neural networks promise to predict molecular properties when plentiful training samples are prepared. 
However, data-hungry problems always stand together with drug-related applications. 
We provide regularization techniques: L2-regularization, dropout and concrete dropout. 
The concrete dropout enables us to avoid manual searching of optimal dropout probabilities for each layer and determine it with optimization process. 

We show the following experimental results:
* Comparison of performances on ML and MAP model estimations
* Comparison of manual dropout searching and of using concrete dropout

### Exp.4 : Uncertainty quantification with Bayesian inference
* Uncertainty quantification of molecular properties
* Comparison of model outputs from MLE and Bayesian inference

### Exp.5 : Improved prediction with transfer learning
* Comparison of training models with and without transfer learning

