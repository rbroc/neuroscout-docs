# Ecosystem

## Overview

Neuroscout is a platform for reproducible fMRI research, encompassing the lifecycle of analysis from model specification to estimation and sharing.

![ecosystem](../static/neuroscout_ecosystem_paths.svg)

The platform is composed of two primary components: __neuroscout.org__: an interactive model builder and data ingestion API; and __Neuroscout-CLI__: an automated model fitting workflow. In addition, __PyNS (Python API)__ supports querying of the API and advanced model creation and model fitting workflows. 


## neuroscout.org

The neuroscout.org server is the key central service in the ecosystem. 

### Analysis Builder
As an end user, you'll use the neuroscout.org analysis builder--an easy-to-use and interactive web application. On neuroscout.org you can [create analyses](../web/builder/intro.md) as well as [browse & manage](../web/builder/intro.md) existing analyses. If you're a first time user, head there to build your first analysis and get started!

### Neuroscout API
These services are supported by the __Neuroscout API__, which makes available all the datasets & predictors through a programmatic interface. The Neuroscout API indexes a curated set of BIDS fMRI datasets, sourced primarily from [OpenNeuro](https://openneuro.org/) & [DataLad](https://datalad.org) repositories. All datasets are [pre-processed](https://github.com/neuroscout-datasets/) and ingested into a SQL database. 

In naturalistic datasets, novel features are extracted from the stimuli using [Pliers](https://www.github.com/PsychoinformaticsLab/pliers)-- an expandable library for feature extraction which spans a wide range of state-of-the-art machine learning algorithms.

The Neuroscout API and Documentation can be accessed at https://neuroscout.org/api/. Access is facilitated in Python by the PyNS library. You can also [browse datasets](https://neuroscout.org/datasets) and [explore predictors](https://neuroscout.org/predictors) on the neuroscout website. 


## Neuroscout-CLI

The [Neuroscout-CLI](../cli/intro.md) is a portable analysis engine which supports the execution of analyses created on neuroscout.org. 

Neuroscout-CLI makes it easy to run your analysis with no configuration by fetching a self-contained analysis bundle, and downloading the required preprocessed fMRI data. Internally, we use [FitLins](https://github.com/poldracklab/fitlins)--a NiPype pipeline for fMRI analysis in BIDS--to fit a statistical model to the fMRI data, and produce comprehensive reports. Neuroscout-CLI automatically uploads the resulting images to Neurovault, and links them to the analysis listing, making it easy to view and share your results.

## pyNS

[pyNS](https://pyns.readthedocs.io/en/latest/) is the Python library for Neuroscout, supporting programmatic access of the Neuroscout API in Python. Serving as the interface for the Neuroscout API, pyNS is used by Neuroscout-CLI to communicate with the Neuroscout server, and push back results to Neurovault. 

Advanced end-users can use pyNS directly instead of the neuroscout.org analysis builder in order to programmaticaly build analyses. This is useful for users that wish to create a large number of analyses, or want to create models which are not supported by the streamlined web-bsed analysis builder. 

As Neuroscout continues to evolve, we aim to support a broader set of models (e.g. encoding models), which may not yet be supported by the Neuroscout analysis builder, or Neuroscout-CLI. pyNS provides the flexibly for developers to create novel workflows such as these, which can later be incorporated upstream as a primary mode of use for the platform.
