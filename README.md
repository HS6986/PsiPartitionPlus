# PsiPartitionPlus
**This repository is currently under construction. Please use PsiPartition instead.**

PsiPartitionPlus is a modified PsiPartition ([xu-shi-jie/PsiPartition](https://github.com/xu-shi-jie/PsiPartition)) ([Xu & Onoda, 2024](https://doi.org/10.1007/s00239-024-10215-7)) with support for binary data and selectivity of whether users will apply ascertainment bias corrections (`+ASC`; [Lewis, 2001](https://doi.org/10.1080/106351501753462876)) to partitions, in the IQ-TREE calculation phases, depending on the conditions of their data.

In my view, applying `+ASC` to a PsiPartition-determined partition in an alignment containing invariant sites that happens to have no invariant sites, which often occurs in the IQ-TREE calculation in PsiPartition, is not justified. It is because such a partition simply reflects the natural condition, rather than being an artificially altered version where invariant sites that should have originally existed are removed.

I thank Dr. Xu and Professor Onoda for developing the innovative software PsiPartition.

Hiroaki Sato  
[hiroaki.biology@gmail.com](hiroaki.biology@gmail.com)

## Installation
```bash
conda create -n PsiPartitionPlus
conda activate PsiPartitionPlus
pip install -r requirements.txt
```

To enable the Bayesian optimization, you need to register an account on [Weights & Biases](https://wandb.ai/).

## Usage
```bash
python PsiPartitionPlus_wandb.py --msa <MSA File> --format <fasta or phylip> --alphabet <dna, aa, or bin> --asc <no or yes> --max_partitions <max_partitions> --n_iter <number of iterations>
```

`--asc` specifies whether `+ASC` should be applied to all partitions or not at all.

## Citation
If you used PsiPartitionPlus in your work, please cite the original PsiPartition paper ([Xu & Onoda, 2024](https://doi.org/10.1007/s00239-024-10215-7)) and the Zenodo repository of PsiPartitionPlus (click `Cite this repository`).
