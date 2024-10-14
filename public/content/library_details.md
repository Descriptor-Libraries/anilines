# Library Details

## Molecule Identification

A list of commercial and substituted aniline (aryl and heteroaryl) building blocks from Thermo Scientific Chemicals (formerly Alfa Aesar chemicals) and Millipore Sigma (formerly Sigma Aldrich) catalogues in 2021. Duplicate molecules were removed. 

## Conformational Searching & Conformer Selection

All calculations were conducted with [Auto-QChem](https://github.com/doyle-lab-ucla/auto-qchem). Three initial conformers were generated with RDKit from SMILES strings, which were subjected to a RMSD threshold of 3.5Å to remove duplicate conformers. The details of conformer generation workflow can be found in the Auto-QChem GitHub repository and the accompanying publication

## DFT Computations

All DFT calculations (Gaussian 16, rev C.01) were performed at the B3LYP/6-31G** level of theory (LANL2DZ was used for atoms heavier than Kr). 
From the DFT calculations, global and atomic properties were extracted with Auto-QChem. The range of properties across the conformational ensemble of a single molecule was summarized by using three measures for each of the properties.


| Descriptors             | Definition                                                                                      |
| ----------------------- | ------------------------------------------------------------------------------------------------|
| Boltz                   | Boltzmann-weighted average of a property from all the conformers in an ensemble (T = 298.15 K)  |
| high_E                  | value of a property from the highest energy conformer in the ensemble                           |
| low_E                   | value of a property from the lowest energy conformer in the ensemble                            |


An extended explanation of the computational workflow used to build the library, as well as details on the collected descriptors can be found in the Auto-QChem GitHub repository and the accompanying publication. 

## Citation
Żurański, A. M.; Wang, J. Y.; Shields, B. J.; Doyle, A. G. React. Chem. Eng. 2022, 7, 1276-1284. Auto-QChem: an automated workflow for the generation and storage of DFT calculations for organic molecules. *React. Chem. Eng.* **2022**, *7*, 1276-1284. DOI: [10.1039/D2RE00030J](https://doi.org/10.1039/D2RE00030J)