
## Input feature 

### Pair frequency
For each pair of columns in the
input alignment, the probability of observing every pair of the 20 canonical amino acids is calculated, with gap characters considered as
an additional amino acid category. Frequencies for unobserved residue pairs are estimated with a pseudocount of 1. Sequence clusters
are weighted based on a 62% sequence identity clustering threshold,
as done for MetaPSICOV input.

##### MetaPSICOV (Jones et al., 2015)
