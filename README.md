# ExaBio
Towards exascale computational bio for genome to function.
An HPC workflow pipleline to infer protein structure from gene sequence, then use structural and bioinformatics tooks to infer function.

## Data


## Software
Here are the links/refs to the software that we intend to use as part of this project.
OpenMM:
https://github.com/openmm/openmm

AMBER version of ExaFold (CPU only), this one is completely functional:
https://github.com/jkwoods/ProteinFoldingPipeline

ExaFold (in progress, uses OpenMM instead of AMBER):
https://github.com/jkwoods/ExaFold


DeepMetaPsiCov: Uses other codes to get info to use a DNN to predict contacts for the protein folding step
Uses Pytorch-- let's see if inference will just run out of the box on GPUs!
Uses CCMPred and other codes that are referenced in the doc
https://github.com/psipred/DeepMetaPSICOV

Protein-protein rigid docking (we are in touch with the dev and want to offload this to GPU):
https://github.com/brianjimenez/lightdock

The PAW workflow manager:
https://github.com/pawtools/nopaw

https://github.com/pawtools/db-launcher
