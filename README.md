## 1. Problem - We want to know the protein structure

### Definition 
* DNA  
* Protein  
* Chain  
* Amino acid  

### Related method
* PSSM  
* PP  
* SS  
* SASA  

### Input data  

Protein | Chain | PSSM | PP | SS | SASA

### Tartget data 

* structure of protein (= angle, position)  
* distance map or contact map  

## 2. related work 

1. Improved protein structure prediction using potentials from deep learning
https://www.nature.com/articles/s41586-019-1923-7
* data : covariation features—the parameters of a regularized pseudolikelihood-trained Potts model (484 features)

2. ResPRE: high-accuracy protein contact prediction by coupling precision matrix with deep residual neural networks   
https://academic.oup.com/bioinformatics/article/35/22/4647/5487385  
-> covariance feature를 이용해  contact-map prediction (deep learning method)

3. hhblits: lightning-fast  iterative protein sequence searching by hmm-hmm alignments
doi:10.1038/nmeth.1818
-> 빠른 msa (alpha fold에서 with Uniclust30 사용)

4. CCMpred—fast and precise prediction of protein residue–residue contacts from correlated mutations
https://doi.org/10.1093/bioinformatics/btu500
-> 1. data와 연관 있음. 

5. https://www.cathdb.info/
-> 1. data만들때 CATH 35% sequence similarity cluster 에서 추출. - 31,247 (keeping all domains from the same homologous superfamily (H-level in the CATH classification)



## 3. evaluation 

1. RMSD  
https://en.wikipedia.org/wiki/Root-mean-square_deviation_of_atomic_positions  

2. TM-score  
https://en.wikipedia.org/wiki/Template_modeling_score

## 4. data

1. MSA (hhblits) -> plmDCA -> input matrix (residu length x residu length x 484)

