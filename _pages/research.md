---
title: "Research"
permalink: /research/
excerpt: "Spectral methods for graph signals, sensor placement under uncertainty, and EEG electrode placement for brain–computer interfaces."
---

My research studies how the structure of signals and measurement systems can guide reliable signal recovery. During my PhD, I worked on the following connected topics.

## Blind separation of graph signals

The graph decorrelation (GraDe) algorithm aims to separate latent graph sources by exploiting the information provided by the graph structure. The method jointly diagonalizes graph autocovariance matrices of the observed mixtures.

We identified a limitation of this method: sample graph autocovariance matrices can be poor estimates of their expected values because graph signal entries are generally neither independent nor identically distributed across nodes (not i.i.d.). The assumptions that justify sample averaging for time signals do not automatically hold for graph signals, so the sample autocovariance matrices of the sources may lack the diagonal structure that GraDe relies on. We showed that outlier eigenvalues in the graph spectrum contribute to this loss of diagonality. The proposed method filters the observed mixtures in the graph spectral domain, removing components associated with outlier eigenvalues, thus improving diagonality and source separation.

**Related paper:** [An improved GraDe method for blind separation of graph signals](https://doi.org/10.1109/TSP.2023.3331264), *IEEE Transactions on Signal Processing*, 2023.

## Sensor placement under uncertainty

Where should sensors be placed to best recover the signals of interest from noisy measurements? We developed a statistical framework that models source-to-sensor gains using Gaussian processes, incorporating uncertainty and prior knowledge into the placement problem.

Criteria based on mean squared error (MSE) and signal-to-interference-plus-noise ratio (SINR) are derived from this model, and sensor locations are optimized using stochastic gradient methods. We also investigated sensor placement for sparse signal reconstruction in underdetermined systems, where both measurement noise and the properties of the sensing matrix influence recovery.


**Related work:** [Signal Processing, 2025](https://doi.org/10.1016/j.sigpro.2024.109659) · [EUSIPCO, 2023](https://doi.org/10.23919/EUSIPCO58844.2023.10289756) · [Manuscript under review]({{ '/publications/#under-review' | relative_url }}).

## EEG and brain–computer interfaces

We applied this framework to EEG electrode placement for P300-based brain–computer interfaces. The model captures differences in source-to-electrode gains between participants and uses shared spatial patterns as prior knowledge.

We proposed a subject-independent electrode placement (SIEP) method that uses this knowledge to choose electrode locations for new participants, reducing the need for full-cap calibration recordings. A hybrid electrode placement (HEP) method incorporates available recordings from the new participant through a Bayesian update, allowing the placement to be tailored to that participant.

I applied this framework to electrode placement for P300-based brain–computer interfaces. The aim is to select useful electrode locations while accounting for variability between people and reducing calibration requirements.

Our subject-independent electrode placement method learns common spatial patterns across a population. A hybrid method combines this prior knowledge with available recordings from a new participant through a Bayesian update.


**Related paper:** [Prior knowledge-driven robust electrode placement method for P300-based brain-computer interfaces](https://doi.org/10.1016/j.bspc.2026.110123), *Biomedical Signal Processing and Control*, 2026.

## Future directions

I am interested in graph machine learning, geometric deep learning, and statistical inference on graphs, especially in understanding their theoretical foundations and developing principled learning methods.
