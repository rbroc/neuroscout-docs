# Overview

The Neuroscout Command Line Interface (_neuroscout-cli_) allows you to execute analyses created on [neuroscout.org](https://neuroscout.org).

_neuroscout-cli_ makes it easy to run your analysis with no configuration by fetching a self-contained analysis bundle, and downloading the required preprocessed fMRI data using [DataLad](https://www.datalad.org/). _neuroscout-cli_ internally uses [FitLins](https://github.com/poldracklab/fitlins), a python pipeline for fMRI analysis in BIDS, to fit a statistical model to the fMRI data, and produce comprehensive reports. _neuroscout-cli_ automatically uploads the resulting images to [Neurovault](https://www.neurovault.org/), and links them to the analysis listing, making it easy to view and share your results.

![fig2b](../static/images/Figure2b.png)

## Getting Started 🚀

If this is your first time running an analysis, follow our interactive guide to [](Neuroscout_CLI_Colab_Demo.ipynb) to run a demo of *Neuroscout-CLI* in the cloud without using any local resources!

```{admonition} Note
Google Colab allows you to execute Jupyer Notebooks for free, using two CPUs for ~6 hours. This should be sufficient for individual Neuroscout analyses. A small demonstration can be run live in ~15 mins, and a normal analysis should execute in a few hours.
```

## Documentation and Reference

[![Documentation Status](https://readthedocs.org/projects/neuroscout-cli/badge/?version=latest&style=flat)](https://neuroscout-cli.readthedocs.io/en/latest/?badge=latest) [![PyPI version](https://badge.fury.io/py/neuroscout_cli.svg)](https://badge.fury.io/py/neuroscout_cli)

For comprehensive reference of _Neuroscout-CLI_ , please visit the official [Neuroscout-CLI Documentation](https://neuroscout-cli.readthedocs.io/en/latest/) on ReadTheDocs. These docs are updated as new Neuroscout-CLI versions are released.


## Installation

The recommended way to install `Neuroscout-CLI` is using containers (i.e. Docker or Singularity) to facilitate dependency managment.

### Containerized Execution

#### Docker

![DockerPulls](https://img.shields.io/docker/pulls/neuroscout/neuroscout-cli.svg)

For most systems (i.e. laptops and workstations), we recommend using [Docker](https://www.docker.com/resources/what-container). 
First, follow the instructions for installing [Docker](https://docs.docker.com/engine/install/) on your system.

Next, follow the [](docker.md) guide in the Neuroscout Docs.

#### Singularity

[Singularity](https://sylabs.io/singularity/) containers are a great solution for High Performance Computing (HPC) environments, where _Docker_ cannot typically be used due to more tightly controlled [user privileges](https://researchcomputing.princeton.edu/support/knowledge-base/singularity).

First, check with your HPC administrator that _Singularity_ is available for use. If so, follow our guide on [](singularity.md) in the offical [Neuroscout Docs](https://neuroscout.org/docs).

### Manually prepared environment using pip

[![PyPI version](https://badge.fury.io/py/neuroscout_cli.svg)](https://badge.fury.io/py/neuroscout_cli)

```{admonition} Danger
Manually installing _neuroscout-cli_ can be difficult due to complex dependencies in the SciPy stack, or fMRI-specific tooling. 
Proceed only if you know what you're doing.
```
Use pip to install _neuroscout-cli_ from PyPI:

    pip install neuroscout-cli