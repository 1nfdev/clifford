[clifford](http://clifford.readthedocs.org/en/latest/): Geometric Algebra for Python
=========================================================

[![PyPI](https://badgen.net/pypi/v/clifford)](https://pypi.org/project/clifford/)
[![DOI](https://zenodo.org/badge/26588915.svg)](https://zenodo.org/badge/latestdoi/26588915)
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/pygae/clifford/master?filepath=examples%2Fg3c.ipynb) 
[![Documentation Status](https://readthedocs.org/projects/clifford/badge/?version=latest)](http://clifford.readthedocs.io/en/latest/?badge=latest)
[![Build Status](https://travis-ci.org/pygae/clifford.svg?branch=master)](https://travis-ci.org/pygae/clifford)
[![Build Status](https://dev.azure.com/hadfieldhugo/clifford/_apis/build/status/pygae.clifford?branchName=master)](https://dev.azure.com/hadfieldhugo/clifford/_build/latest?definitionId=1&branchName=master)
[![codecov](https://codecov.io/gh/pygae/clifford/branch/master/graph/badge.svg)](https://codecov.io/gh/pygae/clifford)

`clifford` is a numerical Geometric Algebra (a.k.a. Clifford algebra) package for python.

- **Documentation:** http://clifford.readthedocs.org
- **Source code:** https://github.com/pygae/clifford
- **Bug reports:** https://github.com/pygae/clifford/issues

Geometric Algebra (GA) is a universal algebra which among several other independent mathematical systems, subsumes:
* Complex numbers
* Quaternions
* Linear algebra

Scalars, vectors, and higher-grade entities can be mixed freely and consistently in the form of mixed-grade multivectors. Like this, 

![blades](https://github.com/pygae/clifford/blob/master/docs/_static/blades.png)


Quickstart
----------

Try out a notebook in [binder](https://mybinder.org/v2/gh/pygae/clifford/master?filepath=examples%2Fg3c.ipynb)

Or have a go on your own pc:
```python
from clifford.g3 import *  # import GA for 3D space
from math import e, pi
a = e1 + 2*e2 + 3*e3 # vector 
R = e**(pi/4*e12)    # rotor 
R*a*~R    # rotate the vector  
```

Syntax Summary
----------

| Syntax  | Operation |
|:-:|:-:|
| \| |  Symetric inner product |
| << |  Left contraction |
|  ^ | Outer product  |
| *  |  Geometric product |
| X\(i\)  |  Return the section of the multivector X of grade i |
| X\(ei\)  |  Return the section of the multivector X for which ei is the pseudo scalar |
| X\[i\]  | Return the i'th coefficient from the multivector X
| X.normal() | Return the normalised multivector so that X*~X is +- 1 |

---

For installation instructions, api documention, and tutorials, [head over to our documentation](https://clifford.readthedocs.io/)!
