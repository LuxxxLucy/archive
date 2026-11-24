# An Active Approach for Interpreting ML Classifier

**An Active Approach for Model Interpretation**

Jialin Lu, Martin Ester

NeurIPS 2019 workshop on Human-centric machine learning (HCML2019)

[An Active Approach for Model Interpretation](https://arxiv.org/abs/1910.12207)

Every computer science project has a two-fold reason for why we do it. The first is why it matters to the real world, in terms of impact and consequences, and the second reason is its ***interestingness*** from a computational viewpoint (after all, we do computer science)

This project is being actively development and have a milestone (A NeurIPS workshop paper) and I am still on further inverstigationss. Feel free to contact me if you're interesting.

- 1. Why it matters to the real world? Model interpretation for pattern discovery.
    
    If a machine learns to predict something, it must learn some knowledge.
    
    - if it could predict better than any other expert system for earthquake after shock prediction, then it must have learn something we do not know.
    - if it could predict better than any man-made tool for predicting drug-response from genomic data, then it must have learn something we do not know.
    
    Then, can we extract that dark knowledge from a machine learning model?
    
    Interpretability has emerged as a crucial aspect of machine learning, aimed at providing insights into the working of, for example, complex deep neural networks. This is essentially important since machine learning based methods are used for simulation of complex systems and inspecting the model provides useful information. 
    
    Recent years we witnessed a trend of deploying deep learning methods in domains like chemistry and biology, where we wish to obtain a highly predictive model and at the same time, we also wish to gain real, real knowledge such as for discovering drug combination effects. Is it possible that we inspect these models for knowledge discovery? This machine learning-based technique has been used for *in silico* simulation, also known as "virtual screening". 
    
    We aim at gaining insights from AI systems, in this time deep neural networks or other machine learning classifier, by extracting the distilled knowledge from the AI system. Now we start with a simple form of IF-ELSE rules.
    
- 2. Why it is interesting from a computational viewpoint.
    
    Normally, model interpretation is formulated as approximating a given model with a simpler, interpretable model. And a straightforward solution, naive but popular, is to apply existing supervised learning methods. 
    
    But we view that, the unique property of model interpretation problem is that we could always generate new desired instance and the query the target model. By doing this, we could get data instances that will help us get better approximation as well as better interpretability, as demonstrated in our work.
    
    So, this insight suggests us to tackle model interpretation, not from a standard supervised learning perspective, but from an active learning perspective. Literally every interpretable model learning algorithm is not designed for active learning, but we could design new algorithms that integrate the active-query part seamlessly with the algorithm that learns an interpretable model.
    
    Which is new, novel and interesting, from a computational perspective.
    

Other Preliminary draft see here:

- Version on August 27th, 2019
    
    [4-page-draft-version.pdf](assets/4-page-draft.pdf)
    
- Version on June the 4th, 2019
    
    [Active Decision Set Induction For Model Interpretation.pdf](assets/active-decision-set-induction.pdf)
