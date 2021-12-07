# Data from DNS, duct flow case

The duct flow case data is from a DNS study from [Pinelli et al. (2010)](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/abs/reynolds-number-dependence-of-mean-flow-structure-in-square-duct-turbulence/64002D5D8E433007E6E359C874C7A44B).

A brief description of the case is pictured below (full description can be consulted [here](https://www.ifh.kit.edu/dns_data/duct/OPEN_duct/doc/data-sheet.pdf)):

## Description of the flow

Incompressible and isothermal fluid in a straight open duct with  a rectangular cross-section. The flow is governed by two parameters, the bulk Reynolds number, and the aspect ratio.

## Numerical method

* Incremental-pressure projection method;
* Crank-Nicholson scheme for the viscous terms;
* Three-step low-storage Runge-Kutta method for the non-linear terms;
* Truncated Fourier series in the streamwise direction (2/3 de-aliasing)
* Chebyshev polynomials in the cross-terms (collocated grid)

## Numerical parameters

* Domain size: L<sub>x</sub> =8πh
* TIme step: CFL ≤ 0.3
* Streamwise grid spacing: Δ≤ 15.2
* Maximun cross-stream grid-spacing max( Δy , Δz) ≤ 4.0
* Statistics accumulated over time *t* ≥ 6000

## Available data

The data-set contains:  

* Components of the time-averaged velocity vector **u**(y,z)
* Components of the Reynolds stress tensor, where the fluctuation is defined as **u'**  


The full data obtained is available [here](https://www.ifh.kit.edu/dns_data/duct/).