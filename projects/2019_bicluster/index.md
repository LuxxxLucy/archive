# Analysis of Critical Modules in Deep Neural Networks

**Checking Functional Modularity in DNN By Biclustering Task-specific Hidden Neurons**

NeurIPS 2019 Neuro↔AI Workshop

Download here the workshop version 

[checking_functional_modularity_in_dnn_by_biclustering_task_specific_hidden_neurons.pdf](assets/functional-modularity-biclustering.pdf)

**A research manuscript** (**The old version) <Dissecting DNN with Co-Adaptive Modules>** 

Downloaded here the research manuscript

[Jialin Lu__Dissecting DNN with Co-Adaptive Modules.pdf](assets/dissecting-dnn-co-adaptive-modules.pdf)

Disclaimer: Fig 1 in the research report is from the Distill Journal.

 

## Brief Summary 👀

---

What is the background for this research?

We hypothesize that like human brain, Deep Neural Networks are also organized in distinct modules for different tasks. A group of neurons could be "functionally" related.

We think it is possible that in a hidden layer, for example 100 neurons, there are 20 neurons that are specified to predict class "A" and there is another 20 neurons for predicting class "B".

We call these 20 neurons a "module", and we find in experiments that the identified modules are rather very sparse.

What is our idea

We seek the dissection of a hidden layer in a pre-trained deep neural network into disjoint groups of hidden neurons that are functionally related for predicting certain sets of similar data samples, i.e. samples with similar feature patterns.

About the approach?

We leverage the feature attribution (or saliency map) methods extended to inner nodes in a hidden layer, such as guided back-prop, DeepLIFT and Integrated-gradient based Conductance value.

Given a pre-trained DNN and a set of data samples, a neuron-sample attribution matrix M is constructed upon which a bi-clustering algorithm is applied.

What do we get?

Our approach provides a way to dissect a hidden layer into functionally related neuron modules in a unsupervised way. These found modules detect different feature patterns and play an important role in predicting samples. Our approach would be very helpful for interpreting DNN’s behavior, and these modules could be directly used to reveal what what feature patterns are learned in the DNN.
