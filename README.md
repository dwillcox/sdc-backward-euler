# SDC ODE Integrator

This is a fourth-order SDC integrator for ODEs for GPUs.

It relies on AMReX for compilation and definition of the Real type.

Uses analytic solution for the sparse linear solve computed with https://github.com/dwillcox/gauss-jordan-solver

The entire integration is run on the GPU in a single kernel to maintain cache locality.

Define AMREX_HOME and then `make`.

Tested with:

- CUDA 9.2.148, gcc 7.4.0, and a Tesla V100
- CUDA 10.0, gcc 7.3, and a Titan V
