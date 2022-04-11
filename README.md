# RiD-feedstock

## Prerequisite
Make sure you have a correct conda environment with conda-build and conda-constructor installed.
Before you start, a new and clean conda environment is recommended.

## How to conda build for rid env

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

## How to install rid_env by installer

just run it using `sh`

```
sh rid-xxx.sh
```

## How to install rid_env by Conda
Note that currently we haven't published this package to public conda channel, but we do release these packages on git release. 

If you want to install modified plumed and groamcs, you should download these two packages from git release. Then add them to a local channel

```
mkdir your_channel
mkdir your_channel/linux-64
# Then you put the packages to the folder you have created.
# cp xxx.tar.bz2 your_channel/linux-64
conda index your_channel

conda install plumed-rid -c file://absolute_path_to_your_channel
```
