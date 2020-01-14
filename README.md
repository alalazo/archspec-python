[![](https://github.com/alalazo/archspec-python/workflows/Unit%20tests/badge.svg)](https://github.com/alalazo/archspec-python/actions)
[![codecov](https://codecov.io/gh/alalazo/archspec-python/branch/master/graph/badge.svg)](https://codecov.io/gh/alalazo/archspec-python)

# Archspec (Python bindings)

Archspec aims at providing a standard set of human-understandable labels for
various aspects of a system architecture  like CPU, network fabrics, etc. and
APIs to detect, query and compare them. 

This project grew out of [Spack](https://spack.io/) and is currently under 
active development. At present it supports APIs to detect and model 
compatibility relationships among different CPU microarchitectures.

## Getting started with development

The `archspec` Python package needs [poetry](https://python-poetry.org/) to
be installed from VCS sources. The preferred method to install it is via 
its custom installer outside of any virtual environment:
```console
$ curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python
``` 
You can refer to [Poetry's documentation](https://python-poetry.org/docs/#installation)
for further details or for other methods to install this tool. You'll also need `tox`
to run unit test:
```console
$ pip install --user tox
```
Finally you'll need to clone the repository: 
```console
$ git clone --recursive https://github.com/alalazo/archspec-python.git
```

### Running unit tests
Once you have your environment ready you can run `archspec` unit tests 
using ``tox`` from the root of the repository:
```console
$ tox
  [ ... ]
  py27: commands succeeded
  py35: commands succeeded
  py36: commands succeeded
  py37: commands succeeded
  py38: commands succeeded
  pylint: commands succeeded
  flake8: commands succeeded
  black: commands succeeded
  congratulations :)
``` 
