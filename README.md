# ExaBio
Towards exascale computational bio for genome to function.
An HPC workflow pipleline to infer protein structure from gene sequence, then use structural and bioinformatics tooks to infer function.

## Data
This section discusses the data for this project.

## Compute
We intend to use various ORNL compute resources such as Summit, CADES, DGX, Raptor etc. 

## Software
Here are the links/refs to the software that we intend to use as part of this project.

OpenMM:
https://github.com/openmm/openmm

AMBER version of ExaFold (CPU only), this one is completely functional:
https://github.com/jkwoods/ProteinFoldingPipeline </br>
^ repo also includes script (and instructions) for generating customizable basic restraints from exsisting PDB files with BioPython.

ExaFold (in progress, uses OpenMM instead of AMBER):
https://github.com/jkwoods/ExaFold


DeepMetaPsiCov: Uses other codes to get info to use a DNN (Deep Neural Network) to predict contacts for the protein folding step
Uses Pytorch-- let's see if inference will just run out of the box on GPUs!
Uses CCMPred and other codes that are referenced in the doc
https://github.com/psipred/DeepMetaPSICOV

Protein-protein rigid docking (we are in touch with the dev and want to offload this to GPU):
https://github.com/brianjimenez/lightdock

The PAW workflow manager:
https://github.com/pawtools/nopaw

https://github.com/pawtools/db-launcher

DNSS secondary structure prediction:
https://github.com/multicom-toolbox/DNSS

## Workflows
This section describes end-to-end workflows that will be enacted as part of this project.

End-to-end stages, workflow 1
1. MSA
2. SSpred
3. CCMpred
4. Build Restrained System
5. ExaFold
6. Run MD to test stability
7. PPI interactions: rigid docking, MD, co-evo hot spots

Meta: coupled learning/ analysis
