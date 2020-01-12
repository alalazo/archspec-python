# archspec-python

Test repository to try a layout based on git submodules. To check out the current repository and try it:
```console
$ git clone --recursive https://github.com/alalazo/archspec-python.git
Cloning into 'archspec-python'...
remote: Enumerating objects: 36, done.
remote: Counting objects: 100% (36/36), done.
remote: Compressing objects: 100% (23/23), done.
remote: Total 36 (delta 10), reused 36 (delta 10), pack-reused 0
Unpacking objects: 100% (36/36), done.
Submodule 'archspec/json' (https://github.com/alalazo/archspec-json.git) registered for path 'archspec/json'
Cloning into '/home/culpo/tmp/archspec/archspec-python/archspec/json'...
remote: Enumerating objects: 4, done.        
remote: Counting objects: 100% (4/4), done.        
remote: Compressing objects: 100% (3/3), done.        
remote: Total 4 (delta 0), reused 4 (delta 0), pack-reused 0        
Submodule path 'archspec/json': checked out '9b582109567e1612b8f9f0494ac720e90c65d269'
```
Once the checkout is done you can install the package using a virtual environment based on Python 3.7:
```console
(py37) $ pip install poetry
[ ... ]

(py37) $ poetry check
All set!

(py37) $ poetry install
Updating dependencies
Resolving dependencies... (6.7s)

Writing lock file


Package operations: 5 installs, 2 updates, 0 removals

  - Updating importlib-metadata (1.1.3 -> 1.4.0)
  - Installing packaging (20.0)
  - Installing pluggy (0.13.1)
  - Installing py (1.8.1)
  - Updating pyrsistent (0.14.11 -> 0.15.7)
  - Installing wcwidth (0.1.8)
  - Installing pytest (5.3.2)
  - Installing archspec (0.1.0)

(py37) $ pytest
============================================================== test session starts ===============================================================
platform linux -- Python 3.7.6, pytest-5.3.2, py-1.8.1, pluggy-0.13.1
rootdir: /home/culpo/tmp/archspec/archspec-python
collected 254 items                                                                                                                              

tests/test_archspec.py .                                                                                                                   [  0%]
tests/test_cpu.py ........................................................................................................................ [ 47%]
.....................................................................................................................................      [100%]

============================================================== 254 passed in 0.69s ===============================================================

(py37) $ poetry build
Building archspec (0.1.0)
 - Building sdist
 - Built archspec-0.1.0.tar.gz

 - Building wheel
 - Built archspec-0.1.0-py3-none-any.whl
```
