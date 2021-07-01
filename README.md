TEME-NTF
=====

This repository implements the non-negative tensor factorization on multi-omics data to deconvolute the epigenetic microenvironment in breast cancer.

## Data

Two datasets were used to model the high-order correlations between signaling proteins, growth ligands and histone modifications:

- RPPA (reverse phase protein array): We downloaded the level3 (log 2 normalized) RPPA data from the [Synapse platform](https://www.synapse.org/#!Synapse:syn12555331).
- GCP (global chromatin profiles): We downloaded the level 3 (log2 normalized) GCP data from the [Synapse platform](https://www.synapse.org/#!Synapse:syn18491838).

We also collected a RNAseq dataset to validate the results produced by our method:

- RNAseq: We downloaded the level 0 (fastq) RNAseq data from the [Synapse platform](https://www.synapse.org/#!Synapse:syn18518040)

## Requirement

  * Python 3.6
  * Numpy
  * Jupyter Notebook

## Usage

1. The significant_test.ipynb implements the Student's t-test for both RPPA and GCP data
2. The NTF_NCP.ipynb implements non-negative tensor factorization on RPPA and GCP tensors using NCP.
3. The NTF_Tensorly.ipynb implements non-negative tensor factorization on RPPA and GCP tensors using Tensorly.

To perform the NTF based on RPPA and GCP data, please run the corresponding notebooks step by step.

## Reference

[1] Kolda, T.G. and Bader, B.W., 2009. Tensor decompositions and applications. SIAM review, 51(3), pp.455-500.

[2] Kim, J., He, Y. and Park, H., 2014. Algorithms for nonnegative matrix and tensor factorizations: A unified view based on block coordinate descent framework. Journal of Global Optimization, 58(2), pp.285-319.

[3] Kossaifi, J., Panagakis, Y., Anandkumar, A. and Pantic, M., 2016. Tensorly: Tensor learning in python. arXiv preprint arXiv:1610.09555.

## Citation

Shi, Min, and Shamim Mollah. "NeTOIF: A Network-based Approach for Time-Series Omics Data Imputation and Forecasting." bioRxiv (2021). doi: https://www.biorxiv.org/content/10.1101/2021.06.05.447209v1.abstract


