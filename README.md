# DeepGS (Graph,Survival): Prognostication of Survival on multiple cancers from RNA sequencing

Introduction:
======

This project is base on the model develop by the DITEP at The Gustave Roussy Institute, DeepOS :https://www.medrxiv.org/content/10.1101/2021.07.10.21260300v1

My project DeepGS is base on this previous project. We strive to predict survival with a new knowlege base on Biologie. An interaction is a reciprocal action between two or more physical systems. An interaction can be materialised in different systems macroscopic or microscopic aspects. In the human body, cancerous organs interact with each other. Cells interact with each other and within these cells proteins interact. In our anatomy, there is a succession of possible interactions. In Deep Learning, we can model the interactions between different genes using Graph Neural Networks.


My project was called.“DeepGS” and its aim were to develop a means to predict a given patient’s survival based on a Multilayer Perceptron by using a new kind of layer. For this l used a dataset based on their genes or organs, and l used several public databases based on protein interactions. In fact, with this protein database, l developed a graph neural network to study interactions between the proteins, whereby this graph was represented by an adjacency matrix. The main idea was to create a Customer Layer to multiply the weight by the adjacency matrix. Indeed, with this point of view, we obtained a new kind of layer that we call a “Graph hidden layer.” l then used this Graph hidden layer in a Multilayer perceptron with a RNA-seq as input. Furthermore, this method describes a new approach that creates a graph neural network for each hidden layer to reduce parameters, avoid overfitting and improve the subsequent step (prediction treatment effect).


Graph Neural Network:
======
![Data Sample](/image/1.png)


Split trainig, test set :
======
![Data Sample](/image/3.png)


Adjacency Matrix Bulding :
======
![Data Sample](/image/4.png)


MLP:
======
![Data Sample](/image/5.png)


With this new layer, we can reduce the weight of information and reduce the parameters. Moreover, this method will allow us to study in the end only the genes with interactions, i.e. the genes for which we have knowledge about the interactions. In this way, we can avoid overfitting and improve the next step of predicting the treatment effect by analysing the different useful interactions.

Graph Hidden Layers:
======
![Data Sample](/image/6.png)


The Deep Learning workflow will be set up in order to reproduce the different interactions present in the immune process with the patient.In order to reproduce biological mechanisms we have created a Deep Learning workflow with four different inputs (T-cells (T.cells.CD8), Macrophages, Neutrophils, Cancer Gene Census). Our workflow will take as hidden layers our Graph Hidden Layers by multiplying the weight with the adjacency matrix.

Deep learning Workflow (parallel neural network):
======
![Data Sample](/image/7.png)

In this part we can observe the results. Cindex is a perfomace index for survial prediction. We got the result withouth and with penalisation. The penalisation method is regularizer l1.

Results:
======
![Data Sample](/image/8.png)







