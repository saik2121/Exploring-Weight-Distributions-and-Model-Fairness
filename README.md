# Exploring-Weight-Distributions-and-Model-Fairness

# Motivation
Pruning on models trained on imbalanced datasets, leads to reduction in the accuracy of the minority class, and increase in the accuracy of the majority class. Previous Studies [[1]](https://arxiv.org/abs/2205.13574) have explored the relation between Gradient norms, Hessians and the size of the minority class.

We explore the relationship between the values of the weights and the reduction in the accuracy of the minority class. To this end we explore two Pruning Options

* L1 Unstructured Pruning (Globally Pruning the weights with the least L1 Norm)
* Our Custom Pruning Method (Globally Pruning the weights with the highest L1 Norm)

# Insights and Observations

We observe that pruning the tail end of the distribution of the weights leads to reduction in the accuracy of the minority class. We rigorously experiment multiple pruning ratios and two different datasets.
For more info, look at our [Wiki Page]()

![img.png](assets/SCR-20231130-lmln.png)
![img_1.png](assets/SCR-20231130-lmsz.png)

# Code
There are two files in the Code/ folder.
* ResNet 18 cifar contains the pruning experiments and the associated results. 
* Module Wise Pruning containes the pruning experiments on custom DNN model and the associated results.

# References
[1. Tran C, Fioretto F, Kim JE, Naidu R. Pruning has a disparate impact on model accuracy. Advances in Neural Information Processing Systems. 2022 Dec 6;35:17652-64.](https://arxiv.org/abs/2205.13574)