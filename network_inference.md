Genetic network inference using hierarchical structure
======================================================
Kimura et al. 2016
------------------

Incorporates a priori knowledge of hierarchical structures exhibited by biochemical networks to improve network inference.

Use hierarchical random graph models of gene networks where:
  + Each leaf node in the hierarchical model corresponds to a node in the original gene regulatory network
  + Internal nodes in the hierarchical model correspond to relationships among the nodes of the original gene regulatory network
  + Each internal node in the hierarchical model is assigned a probability
  + That probability corresponds to the probability that leaf nodes which have that internal node as their lowest common ancestor have an edge between them in the original gene regulatory network
  + e.g. When the leaf nodes *u* and *v* have the internal node *D_i* as their lowest common ancestor, it means that the original gene regulatory network has an edge between *u* and *v* with the probability *theta_i*

The approach relies on being able to infer a number of gene regulatory networks, which you then use to infer a single hierarchical random graph model.

In this study, they used the hierarchical random graph model to rank equally likely interactions inferred using a separate approach called bootstrap LPM.
