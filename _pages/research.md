---
title: "Research"
permalink: /research/
excerpt: "Spectral methods for graph signals, sensor placement under uncertainty, and EEG electrode placement for brain–computer interfaces."
---

The following sections provide an overview of my doctoral research ([PhD defense slides]({{ '/files/phd-defense-slides.pdf' | relative_url }})). My PhD thesis will be public soon; [contact me](mailto:{{ site.author.email }}) for a copy.

## Graph signal separation

The graph decorrelation (GraDe) algorithm aims to separate latent graph sources by exploiting the information provided by the graph structure. The method jointly diagonalizes graph autocovariance matrices of the observed mixtures.

We identified a limitation of this method: sample graph autocovariance matrices can be poor estimates of their expected values because graph signal entries are generally neither independent nor identically distributed across nodes (not i.i.d.). Stationarity and ergodicity assumptions for time signals do not automatically extend to graph signals, so source sample autocovariance matrices may lack the diagonality required by GraDe. We showed that outlier eigenvalues in the graph spectrum contribute to this loss of diagonality. The proposed method filters the observed mixtures in the graph spectral domain, removing components associated with outlier eigenvalues, thus improving diagonality and source separation.

**Related paper:** [An improved GraDe method for blind separation of graph signals](https://doi.org/10.1109/TSP.2023.3331264), *IEEE Transactions on Signal Processing*, 2023.

## Sensor placement under uncertainty

Where should sensors be placed to best recover the signals of interest from noisy measurements? We developed a statistical framework that models source-to-sensor gains using Gaussian processes, incorporating uncertainty and prior knowledge into the placement problem.

Criteria based on mean squared error (MSE) and signal-to-interference-plus-noise ratio (SINR) are derived from this model, and sensor locations are optimized using stochastic gradient methods. We also investigated sensor placement for sparse signal reconstruction in underdetermined systems, where both measurement noise and the properties of the sensing matrix influence recovery.


**Related work:** [Signal Processing, 2025](https://doi.org/10.1016/j.sigpro.2024.109659) · [EUSIPCO, 2023](https://doi.org/10.23919/EUSIPCO58844.2023.10289756) · [Manuscript under review]({{ '/publications/#under-review' | relative_url }}).

## EEG and brain–computer interfaces

An objective in EEG-based systems is to use fewer electrodes without sacrificing accuracy. The challenge is that finding optimal locations for those few electrodes often requires calibration recordings from many electrodes first. We addressed this challenge in P300-based brain–computer interfaces (BCIs) through stochastic modeling of P300 gains, capturing variability across participants and learning shared spatial patterns as prior knowledge for electrode placement.

The proposed subject-independent electrode placement (SIEP) method uses this prior knowledge to select optimal electrode locations without any calibration recordings, transferring learned knowledge robustly across population datasets. Hybrid electrode placement (HEP) tailors the placement to a new participant by incorporating available recordings through a Bayesian update.

**Related paper:** [Prior knowledge-driven robust electrode placement method for P300-based brain-computer interfaces](https://doi.org/10.1016/j.bspc.2026.110123), *Biomedical Signal Processing and Control*, 2026.

## Future directions

I am interested in graph machine learning, geometric deep learning, and statistical inference on graphs, especially in understanding their theoretical foundations and developing principled learning methods.
