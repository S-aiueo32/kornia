.. raw:: html

  <p align="center">
    <img width="50%" src="https://github.com/arraiyopensource/kornia/blob/master/docs/source/_static/img/kornia_logo.svg" />
  </p>

--------------------------------------------------------------------------------

.. image:: https://circleci.com/gh/arraiyopensource/kornia/tree/master.svg?style=svg
    :target: https://circleci.com/gh/arraiyopensource/kornia/tree/master

.. image:: https://codecov.io/github/arraiyopensource/kornia/branch/master/graph/badge.svg
    :target: https://codecov.io/github/arraiyopensource/kornia

.. image:: https://badge.fury.io/py/kornia.svg
    :target: https://badge.fury.io/py/kornia

.. image:: https://readthedocs.org/projects/kornia/badge/?version=latest
    :target: https://kornia.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation Status

*Kornia* is a differentiable computer vision library for `PyTorch <https://pytorch.org/>`_.

It consists of a set of routines and differentiable modules to solve generic computer vision problems. At its core, the package uses *PyTorch* as its main backend both for efficiency and to take advantage of the reverse-mode auto-differentiation to define and compute the gradient of complex functions.

Overview
========

Inspired by *OpenCV*, this library is composed by a subset of packages containing operators that can be inserted within neural networks to train models to perform image transformations, epipolar geometry, depth estimation, and low-level image processing such as filtering and edge detection that operate directly on tensors.

At a granular level, Kornia is a library that consists of the following components:

+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| **Component**                                                              | **Description**                                                                                                                       |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| `kornia <https://kornia.readthedocs.io/en/latest/index.html>`_             | a Differentiable Computer Vision library like OpenCV, with strong GPU support                                                         |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| `kornia.color <https://kornia.readthedocs.io/en/latest/color.html>`_       | a set of routines to perform color space conversions                                                                                  |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| `kornia.contrib <https://kornia.readthedocs.io/en/latest/contrib.html>`_   | a compilation of user contrib and experimental operators                                                                              |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| `kornia.feature <https://kornia.readthedocs.io/en/latest/feature.html>`_   | a module to perform feature detection                                                                                                 |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| `kornia.filters <https://kornia.readthedocs.io/en/latest/filters.html>`_   | a module to perform image filtering and edge detection                                                                                |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| `kornia.geometry <https://kornia.readthedocs.io/en/latest/geometry.html>`_ | a geometric computer vision library to perform image transformations, 3D linear algebra and conversions using different camera models |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| `kornia.losses <https://kornia.readthedocs.io/en/latest/losses.html>`_     | a stack of loss functions to solve different vision tasks                                                                             |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+
| `kornia.utils <https://kornia.readthedocs.io/en/latest/utils.html>`_       | image to tensor utilities and metrics for vision problems                                                                             |
+----------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------+

Installation
============

**From pip:**

.. code:: bash

    pip install kornia

**From source:**

.. code:: bash

    python setup.py install

**From source using pip:**

.. code:: bash

    pip install git+https://github.com/arraiyopensource/kornia

Quick Usage
===========

.. code:: python

 import torch
 import kornia

 x_rad = kornia.pi * torch.rand(1, 3, 3)
 x_deg = kornia.rad2deg(x_rad)

 torch.allclose(x_rad, kornia.deg2rad(x_deg))  # True

Examples
========

Run our Jupyter notebooks `examples <https://github.com/arraiyopensource/kornia/tree/master/examples/>`_ to learn to use the library.


Cite
============

If you are using kornia in your research-related documents, it is recommended that you cite the poster.

.. code:: bash

 @misc{Arraiy2018,
  author    = {E. Riba, M. Fathollahi, W. Chaney, E. Rublee and G. Bradski}
  title     = {torchgeometry: when PyTorch meets geometry},
  booktitle = {PyTorch Developer Conference},
  year      = {2018},
  url       = {https://drive.google.com/file/d/1xiao1Xj9WzjJ08YY_nYwsthE-wxfyfhG/view?usp=sharing}
 }


Contributing
============
We appreciate all contributions. If you are planning to contribute back bug-fixes, please do so without any further discussion. If you plan to contribute new features, utility functions or extensions, please first open an issue and discuss the feature with us. Please, consider reading the `CONTRIBUTING <https://github.com/arraiyopensource/kornia/blob/master/CONTRIBUTING.rst>`_ notes. The participation in this open source project is subject to `Code of Conduct <https://github.com/arraiyopensource/kornia/blob/master/CODE_OF_CONDUCT.md>`_.
