# PsiPartitionPlus
PsiPartitionPlus is a modified PsiPartition ([xu-shi-jie/PsiPartition](https://github.com/xu-shi-jie/PsiPartition)) ([Xu & Onoda, 2024](https://doi.org/10.1007/s00239-024-10215-7)) with support for binary data and selectivity of whether users apply ascertainment bias corrections (`+ASC`) ([Lewis, 2001](https://doi.org/10.1080/106351501753462876)) to partitions, in the IQ-TREE calculation phase, depending on the conditions of their data.  
  
In my view, applying `+ASC` to a PsiPartition-determined partition in an alignment containing invariant sites that happens to have no invariant sites, which often occurs in the IQ-TREE calculation in PsiPartition, is not justified. It is because such a partition simply reflects the natural condition, rather than being an artificially altered version where invariant sites that should have originally existed are removed.  
  
This repository is currently under development, and its content is exactly the same as PsiPartition.  
  
I thank Dr. Xu and Professor Onoda for developing the innovative software, PsiPartition.  
  
Hiroaki Sato (he/him)  
Senior High School at Komaba, University of Tsukuba  
4-7-1 Ikejiri, Setagaya-ku, Tokyo 154-0001, Japan  
[hiroaki.biology@gmail.com](hiroaki.biology@gmail.com)  
________________________________________________________________________
![](logo.png)

This is the official implementation of the paper "PsiPartition: Improved Site Partitioning for Genomic Data by Parameterized Sorting Indices and Bayesian Optimization" [Journal of Molecular Evolution](https://link.springer.com/article/10.1007/s00239-024-10215-7).

## Installation

```bash
conda create -n PsiPartition
conda activate PsiPartition
pip install -r requirements.txt
```

To enable the Bayesian optimization, you need to register an account on [Weights & Biases](https://wandb.ai/).
## Usage

```bash
python PsiPartition_wandb.py --msa <MSA File> --format <fasta or phylip> --alphabet <dna or aa> --max_partitions <max_partitions> --n_iter <number of iterations>
```

## Help
If you have any questions, please contact me at `shijie.xu@ees.hokudai.ac.jp`.
