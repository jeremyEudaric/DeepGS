# DeepGS: Prognostication of Survival on multiple cancers from RNA sequencing

Introduction:
======

This project is base on the model develop by the DITEP at The Gustave Roussy Institute, DeepOS :https://www.medrxiv.org/content/10.1101/2021.07.10.21260300v1

My project DeepGS is base on this previous project, we strive predict survival with a new knowlege base on Biologie. An interaction is a reciprocal action between two or more physical systems. An interaction can be materialised in different systems macroscopic or microscopic aspects. In the human body, cancerous organs interact with each other, cells interact with each other and within these cells proteins interact. In our anatomy, there is a succession of possible interactions. In Deep Learning, we can model the interactions between different genes using Graph Neural Networks. 

My project  was called “DeepGS” and its  aim was  to develop a means to predict  a given patient’s survival based on a Multilayer Perceptron  by using a new kind of layer. For this l used a dataset based on their genes or organs, and l used several public databases based on protein  interactions. In fact, with this protein database, l developed  a graph neural network to  study interactions between the proteins, whereby this graph was  represented by an adjacency matrix. The main idea was  to create a Customer Layer to multiply the weight by the adjacency matrix. Indeed, with this point of view , we obtained  a new kind of layer that we call a “Graph hidden layer”.  l then used this Graph hidden layer in a Multilayer perceptron with an RNA-seq as input. Furthermore, this method  describes a new approach  that creates a graph neural network for each hidden layer to reduce parameters, avoid overfitting and improve the subsequent step (prediction treatment effect). 

![Data Sample](/images/1.png)
