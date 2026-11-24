# Functional Parcellation in Brain Images

**A Research manuscript**

The research report <K-parcel: Spatially-Continuous Brain Parcellation> could be downloaded here.

[K-parcel Spatially-Continous Brain Parcellation.pdf](assets/k-parcel.pdf)

This is an unpublished manuscript and is considered as **an exercise of research skill learning** for my master's research supervised by Prof. Martin Ester and Prof. Maxwell Libbrecht.

**A meta comment**: 

the proposed approach is somehow similar to the work of ReNA 

[Recursive nearest agglomeration (ReNA): fast clustering for approximation of structured signals](https://arxiv.org/abs/1609.04608)

This paper shares the same intuiton but is much better than my work, in many aspects, and is rigorously evaluated. And it is fast.

*Hoyos-Idrobo et al, 2019, IEEE transactions of on Pattern Analysis and Machine Intelligence* 

## Brief

---

Functional parcellation purposes to divide a spatial activity map, such as brain images, into homogeneous and functionally coherent regions, which serve with fundamental importance as applications to analysis and interpretation.

Previous practice on this task choose to do clustering in the feature space while ignoring the spatial proximity, and consider features by calculating simple statistical measure such as correlation. We argue that those widely adopted clustering methods often results in not spatially continous and unsatisfactory parcellations in inevitable noisy settings in brain images, questioning the reliability of parcellation.

## Context and The "Gap" 👀

---

what this research is about:

Traditional anatomy-based brain parcellations often fail to capture he intrinsic functional coherence and thus comes the rise of data-driven parcellation methods based on clustering algorithms.

However, Current clustering algorithm is not good enough and in terms of the main evaluation metrics, algorithms generally give contrast results in different metrics: a algorithm performs well in one metric and give poorest performance in another metric. There is no algorithm that could **satisfy all these metrics at the same time**. 

And One very important issue is that, existing method are especially **fragile to noise** which is inherent in current brain imaging technology. 

## Our approach

---

We propose K-parcel, a simple clustering algorithm which could be viewed as a constrained K-means that guarantee to obtain spatially-connected and highly coherent functional parcellations on a spatial activity map. K-parcel is able to group voxels with coherent feature
patterns and robust to noisy signals which leads to the aforementioned problems in practice.

The proposed method is compared with several alternative approaches through simulation studies, and is applied to real brain images. Experimental results demonstrate the superiority and robustness of K-parcel algorithm that it could find spatially-connected and homogeneous parcellation even in high noisy settings.

## Compared methods

---

We compare our methods to these existing methods (please refer to the research report if there are any conflicts here)

- K-means (still the best and most robust clustering algorithm) with PCA
    
    transform timeseries by PCA and cluster based on these features plus spatial coordinates.
    
- K-means with spatial regularization weighting
- K-means using correlation with whole brain background as feature
    
    Thorsten Kahnt 2012
    
    [Kahnt et al. 2012, Journal of Neuroscience (PDF)](http://www.jneurosci.org/content/jneuro/32/18/6240.full.pdf)
    
- Ward's Algorithm: merge clusters by variance-minimizing.
    
    
- N-cuts: normalized cut spectral clustering
    
    The most natural way to start is the N-cuts as shown in
    
    [A human brain atlas derived via n-cut parcellation of resting-state and task-based fMRI data. - PubMed - NCBI](https://www.ncbi.nlm.nih.gov/pubmed/26523655)
    
     and this is the original normalized cuts paper
    
    [Normalized Cuts and Image Segmentation](https://dl.acm.org/citation.cfm?id=351611)
    
- Spectral K-means clustering
    1. construct the graph of both spatial adjcency and connectivity.
    2. take the first k=100 eigenvectors of such matrix
    3. perform K-means

Brief review on the results which are consistently yield in two survey paper. In two of the main evaluating metrics:

- **Reproducibility**: N-cuts shows good reproducibility among subjects, while k-means and Ward's give poor performance
- **Parcel Homogeneity**: K-means outperform all others (both homogenetity and Silhouette scores), followed by hierachical approaches. N-cuts shows the poorest result.

## Important Reference 🌝

---

Important materials for the research project

two important survey paper with systematic comparision

[Which fMRI clustering gives good brain parcellations?](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4076743/)

Which fMRI clustering gives good brain parcellations

By Bertrand Thirion et al. 2014

[fnins-08-00167.pdf](assets/fnins-08-00167.pdf)

- notes
    
    K-means, Ward, Spectral clustering are compared on synthetic and two real datasets.
    
    There are two metrics where those methods show diverge performance.
    
    1. Accuracy (parcel homogeneity)
    2. Stability (Reproducibility among different subjects)

[Human brain mapping: A systematic comparison of parcellation methods for the human cerebral cortex. - PubMed - NCBI](https://www.ncbi.nlm.nih.gov/pubmed/28412442)

Human brain mapping: A systematic comparison of parcellation methods for the human cerebral cortex

By Arslan Salim et al. 2018

[1-s2.0-S1053811917303026-main.pdf](assets/arslan-2018-parcellation-comparison.pdf)

- notes

these two papers provide good insights on how to evaluate good brain parcellation methods and also comprehensive comparision of many clustering methods.

Yet another important reference is this one which explains a lot about the signal-to-noise ratio of fMRI data

**On the Definition of Signal-To-Noise Ratio and Contrast-To-Noise Ratio for fMRI Data**

By Marijke Welvaert et al. 2013

[On the Definition of Signal-To-Noise Ratio and Contrast-To-Noise Ratio for fMRI Data](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0077089)

[journal.pone.0077089.PDF](assets/pone-0077089.pdf)
