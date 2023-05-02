**<span style="font-variant:small-caps;">Tolosa</span>** is a research project to develop an efficient open source simulation software for free surface flow, especially for marine flooding previsions, including wave modeling using new Boussinesq-type model and associated numerical resolution.

The main contributions are the software layer the mathematical background to propose efficient simulations considering unstructured grids, much more flexible and efficient to consider complex shorelines and to adapt the size cells to the physics wanted to be capture.

It is implemented original numerical schemes with:
* global stability by entropy dissipation.
* low dissipation, especially in high frequencies.
* respect to the asymptotic low Froude number property.

The software is developed in [Fortran 2008](http://fortranwiki.org) with a [KISS principle](https://en.wikipedia.org/wiki/KISS_principle) (Keep It Stupid and Simple) and with some [OOP](https://en.wikipedia.org/wiki/Object-oriented_programming) (Object-oriented programming) features.

A library called **<span style="font-variant:small-caps;">Tolosa-lib</span>** is used at the top to numerically solve each model on unstructured meshes in a CPU MPI parallel environment. It mainly includes:
 * the mangement of partionned unstructured meshes taking care to data locality for enhanced computation speed.
 * some structures to handle as simply as possible the Inputs/Ouputs in parallel including list of parameters, command line interface, VTK, Tecplot, Yaml, CSV, etc ...
