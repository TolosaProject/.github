**<span style="font-variant:small-caps;">Tolosa</span>** is a research project aimed at developing efficient open-source simulation software for free-surface flows, in particular for marine flood forecasting, including wave modeling using a new Boussinesq-type model and the associated numerical resolution.

The main contributions are the software layer and the mathematical background to propose efficient simulations considering unstructured grids, which are much more flexible and efficient to account for complex coastlines and to adapt the cell size cells to the physics to be captured.

It is implemented original numerical schemes with:
* global stability by entropy dissipation.
* low dissipation, especially at high frequencies, in relation to the computing costs.
* respect to the asymptotic low Froude number property.

The software was developed in [Fortran 2008](http://fortranwiki.org) according to the [KISS principle](https://en.wikipedia.org/wiki/KISS_principle) (Keep It Stupid and Simple) and with some [OOP](https://en.wikipedia.org/wiki/Object-oriented_programming) (object-oriented programming) features.

A library called **<span style="font-variant:small-caps;">Tolosa-lib</span>* is used at the top to numerically solve any model on unstructured meshes in a parallel CPU-MPI environment. It mainly includes:
 * the management of partitioned unstructured meshes considering the data locality to increase the computation speed.
 * some structures to handle the inputs/outputs in parallel as easily as possible, including parameter list, command line interface, VTK, Tecplot, Yaml, CSV, etc ...
