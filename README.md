# Stardist Conda Environments

This repository hosts `.yml` files to create conda/mamba environments with [stardist](https://github.com/stardist/stardist), [napari](https://napari.org/stable/) and [pyclesperanto](https://github.com/clEsperanto/pyclesperanto_prototype).

## Usage

* [Linux](#linux)
* [Windows](#windows)

### Linux

1. Download and install [mambaforge](https://github.com/conda-forge/miniforge#mambaforge) for Linux.

    * (optional) In case you have [miniforge or miniconda](https://github.com/conda-forge/miniforge#miniforge3) already installed, you can install `mamba` in the `base` environment with `conda install -c conda-forge mamba`.

2. From a terminal, run `mamba init` once, close that terminal and open a new one.

3. Download the [`stardist-linux.yml`](https://github.com/BiAPoL/stardist-envs/blob/main/stardist-linux.yml) file from this GitHub repository (right-click on 'Raw' and 'Save link as...').

4. In the new terminal, navigate to the place where you saved `stardist-linux.yml` and run:

    `mamba env create -f stardist-linux.yml`
    
5. Activate the new environment with:

    `mamba activate stardist-linux`
    
6. From the activated environment, run the following lines to set the system path (for more information, check [here](https://www.tensorflow.org/install/pip#linux_1)):

    `mkdir -p $CONDA_PREFIX/etc/conda/activate.d`
    
    `echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/' > $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh`
    
    `echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/python3.8/site-packages/tensorrt/' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh`
    
7. Clone the [Stardist repository](https://github.com/stardist/stardist) to your computer (using [GitHub Desktop](https://desktop.github.com/) for example or `git` commands).

8. Run/modify the example notebooks to your needs through `jupyter lab` (optionally, open [napari](https://napari.org/stable/) and use the [stardist-napari plugin](https://www.napari-hub.org/plugins/stardist-napari)).

### Windows

1. Download and install [mambaforge](https://github.com/conda-forge/miniforge#mambaforge) for Windows.

    * (optional) In case you have [miniforge or miniconda](https://github.com/conda-forge/miniforge#miniforge3) already installed, you can install `mamba` in the `base` environment with `conda install -c conda-forge mamba`.

2. Download the [`stardist-windows.yml`](https://github.com/BiAPoL/stardist-envs/blob/main/stardist-windows.yml) file from this GitHub repository (right-click on 'Raw' and 'Save link as...').

3. In the new terminal, navigate to the place where you saved `stardist-windows.yml` and run:

    `mamba env create -f stardist-windows.yml`
    
4. Activate the new environment with:

    `mamba activate stardist-windows`
    
5. Clone the [Stardist repository](https://github.com/stardist/stardist) to your computer (using [GitHub Desktop](https://desktop.github.com/) for example or `git` commands).

6. Run/modify the example notebooks to your needs through `jupyter lab` (optionally, open [napari](https://napari.org/stable/) and use the [stardist-napari plugin](https://www.napari-hub.org/plugins/stardist-napari)).
    
