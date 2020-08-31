* Improving prediction of protein secondary structure, 
backbone angles, solvent accessibility and contact numbers 
by using predicted contact maps and an ensemble of recurrent 
and residual convolutional neural networks
-> (Spider3) [https://pubmed.ncbi.nlm.nih.gov/30535134/]


1. Input feature 
* PSSM : 20 (PSI-BLAST against the UniRef90 sequence database updated in April 2018)
* PP : 7 (physicochemical properties of each amino acid, such as Van der Waal’s volume and polarizability)
* Residue substitution values : 20
* transition frequency and the number of effective homologous sequences : 10  
-> Total : 57
* Contact prediction (SPOT-Contact, t only predicts contacts for residues that are greater than or equal to 3 in sequence position separation) 

2. Output 

* ASA
* HSEa-up and -down
* CN, 
* Sin(theta) & Cos(theta) 
* Sin(tau) & Cos(tau)
* Sin(phi) & Cos(phi)
* Sin(psi) & Cos(psi)  
-> Total : 12

3. Ground truth 
* SS3, SS8, ASA and phi and psi angles from their PDB file (DSSP)

4. Dataset
* 12,450 proteins from the PISCES server on Feb 2017 with the constraints of high resolution (<2.5A˚ ), an R-free <1
* sequence identity cutoff of 25% according to BlastClust.
* 1250 proteins deposited after June 2015 were separated into a test set, leaving 11200
* proteins which were randomly divided into a train set (10,200 proteins) and validation set (1000). 
* As in SPOT-Contact we removed
the proteins over 700 residues in the above training, validation and
test sets for efficient calculations. This reduces our training, validation and independent test sets to 10 029, 983 and 1213 proteins,
respectively

* Test set 
*  structures from the PDB released between 01/01/2018 and 07/16/2018
* resolution < 2.5A˚ and R-free < 0.25
* proteins with >25% sequence identity to structures released prior to 2018.
* d to remove redundancy at a 25% sequence identity cutoff.

->
TEST2016 (1213 proteins) and TEST2018 (250 proteins) as they
were deposited between June 2015 and Feb 2017 and between Jan
2018 and July 2018, respectively. For a measure of our predictor on
a harder set, we employ the TEST-HARD set from Hanson et al.
(2018), a subset of TEST2016 after removing proteins with a Blast
E-value of <0.1 against our Train set. In addition, we utilize 20
available Template-Free Modelling (TFM) proteins from CASP12
(Schaarschmidt et al., 2018) for independent testing of the available
methods (CASP12). This set has < 25% sequence similarity to our
training set.
