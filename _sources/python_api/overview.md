# Usage & Reference

[![Documentation Status](https://readthedocs.org/projects/pyns/badge/?version=latest&style=flat)](https://pyns.readthedocs.io/en/latest/?badge=latest) [![PyPI version](https://badge.fury.io/py/pyNS.svg)](https://badge.fury.io/py/pyNS)

__pyNS__ is the Python client library for accessing the [Neuroscout API](https://neuroscout.org/api).

At it's most basic, __pyNS__ facilitates making HTTP requests to the API, by pre-formulating requests, and making it accessible via an easy-to-use, Pythonic API. In addition, __pyNS__ supports Neuroscout applications that interact with the API, such as [Neuroscout-CLI](../cli/intro.md).

For the end user, __pyNS__ enables flexibly querying and interaction with the Neuroscout API, enabling several advanced cases not supports by the web-based application such as:


* Downloading data from Neuroscout, including full predictor time courses
* Batch-creation of analyses-- particular useful for meta-analytic workflows which test the same analysis across datasets
* Full flexiblity in specification of [BIDS StatsModels](https://bids-standard.github.io/stats-models/). This enables statistical models which may not be supported by the web app, but are valid and executable models.

In addition, for developers __pyNS__ may enable the development of novel experimental applications that use Neuroscout API's data. For example, there is ongoing work to develop an encoding analysis workflow in Neuroscout using __pyNS__. 

## Quickstart
For comprehensive reference of `pyNS` usage (including [quickstart](https://pyns.readthedocs.io/en/latest/quickstart.html), [querying](https://pyns.readthedocs.io/en/latest/querying.html) & [creating analyses](https://pyns.readthedocs.io/en/latest/analyses.html)) and [Python API](https://pyns.readthedocs.io/en/latest/api.html) reference, please visit the official [pyNS Documentation](https://pyns.readthedocs.io/en/latest/) on ReadTheDocs. These docs are updated as new pyNS versions are released.

## Contribute to pyNS

If you'd like to conribute to pyNS, visit the [pyNS repository](https://github.com/neuroscout/pyns) on GitHub.
For bug reports or feature requests, please [submit an issue](https://github.com/neuroscout/pyns).