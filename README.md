# RiD-feedstock

## Prerequisite
Make sure you have a correct conda environment with conda-build and conda-constructor installed.
Before you start, a new and clean conda environment is recommended.

## Usage

```
# activate new conda env
conda activate YOUR_ENV

cd plumed-rid-xxx
conda build . -c conda-forge

cd gromacs-rid-xxx
conda build . -c conda-forge -c file://path_to_plumed_install_package
# path_to_plumed_install_package usually is /opt/conda/xxx/conda-bld

cd installer
constructor .
```
