# High precision in protein contact prediction using fully convolutional neural networks and minimal sequence features

## Input feature 

### Pair frequency
For each pair of columns in the input alignment, the probability of observing every pair of the 20 canonical amino acids is calculated, with gap characters considered as an additional amino acid category. Frequencies for unobserved residue pairs are estimated with a pseudocount of 1. Sequence clusters are weighted based on a 62% sequence identity clustering threshold,as done for MetaPSICOV input.

##### by MetaPSICOV (Jones et al., 2015)

### Covariance 
Using marginal and pair frequencies for each pair of amino acids as described above, we calculate the covariance between every pair of residues at every pair of sites, and use these as an alternative set of input features.

-> For a given pair of amino acid types, pair frequencies or covariances are composed as an mxm matrix, where m is the number of columns in the sequence alignment. Considering 20 amino acid typesþ gap, there are 21x21 = 441 

### Input matrix = 441 x m x m 
(number of columns in the sequence alignment = m) 
({every pair of the 20 canonical amino acids + gap characters} = 21) 
(21 x 21 = 441) 
