##  Projects

### *Taichi*
Taichi is a FMM based collisional dynamics *N*-body code that is optimized to handle million and post-million body problems. The code is built on top of exaFMM with changes made to improve the force accuracy and optimizations for collisional dynamics. For accurate few-body dynamics, regularization is included. Work is in progress to implement post-Newtonian effects and gravitational wave recoil. *Taichi* includes time-symmetrized hamiltonian splitting integrators of second and fourth orders. For the latter, gradient extrapolation based forward symplectic methods are used to avoid negative timesteps and improve accuracy.

### *Falcon*
*Falcon* is a custom *N*-body code that is tuned to simulate intermediate mass ratio inspirals embedded in dark matter spikes. Since the self-gravity of the spike in minimal, *Falcon* neglects DM-DM interactions which speeds up the simulation. Post-Newtonian effects upto 2.5 order are included and work is in progress to implement post-Newtonian effects upto 3.5 order. Integration is performed using a second order auxiliary variable based method since the post-Newtonian Hamiltonian is non-separable. It includes adaptive timestepping via the usage of time-symmetrized methods to improve accuracy.

### Evolution of Primordial Solar System

Using two coupled astrophysical codes, _rebound_ and _NBODY6++_, my collaborators at Leiden University and I explored the effects of the Sun's birth cluster on the dynamics of the giant planets and the secular evolution of the debris disk surrounding the planets. 

### [*PyStarsmasher*](https://github.com/dipto4/PyStarsmasher)

For my bachelor's thesis, I created a new Python based interface for smoothed particle hydrodynamics (SPH) code _Starsmasher_ which is used for studying stellar mergers. The new interface/code, named _PyStarsmasher_, can be coupled with any other astrophysical code using the Python interface. One can imagine coupling it to gas dynamics or gravitational dynamics codes using AMUSE. _PyStarsmasher_ is an open-source code and can be downloaded [here](https://github.com/dipto4/PyStarsmasher).

### Formation of Runaway Collision Objects

For my bachelor's thesis, I devised a novel method to study stellar collisions in _NBODY6++_ using _Starsmasher_ using _PyStarsmasher_. This method of coupling codes had not been used before and provided better results while treating stellar mergers in star clusters. This coupled code was then used to study the formation of runaway collision objects in star clusters. 

### [*NBODY6++*](https://github.com/dipto4/NBODY6_collision_detection)

For my bachelor's thesis, I had to work with _NBODY6++_. I worked to modify the original code to allow for collisions to take place even when stellar evolution is switched off. In addition to that, the new code outputs details of all stars in the cluster for multiple timesteps before a collision has taken place so that it can be tracked. These files can be read using _PyStarsmasher_ to set up a sequence of collisions. The modified code can be found
[here](https://github.com/dipto4/NBODY6_collision_detection).
