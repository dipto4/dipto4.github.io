---
layout: default
---

## About me

I am a computational astrophysicist pursuing my Ph.D. in physics at Carnegie Mellon University. I graduated *summa cum laude* with a  Bachelor of Science in physics along with minors in economics and computer science from Allegheny College in 2019. 

My work lies at the intersection of numerical methods development and gravitational dynamics. I have been involved in the development of fast force calculation techniques to speed up simulations of large stellar and galactic systems to study the mergers of massive black hole binaries. In particular, my collaborators and I have developed a collisional *N*-body code called *Taichi* which uses a finely tuned and optimized fast multipole method (FMM) based force solver. I have also been actively involved in the development and implementation of various novel integration and timestep methods that help preserve the symplectic and time symmetric properties of the Hamiltonian.   
My background is quite diverse having worked in a variety of projects at various scales - solar system dynamics, stellar dynamics in young massive clusters, and combining hydrodynamics with gravitational dyanmics for clusters.

I am proficient in Fortran (77,90), C/C++, and Python. While *Taichi* is parallelized using openMP, I have previously worked with CUDA and MPI.

On the computer science side of things, I am interested in high performance computing (HPC), GPU computing, and machine learning (ML). I have worked with Generative Adversarial Networks (GANs) to simulate galaxy images for future galaxy surveys and symbolic regression to implement new force softening techniques in cosmological simulations.


Outside of academics, I am involved in a variety of things. I was the president of the Astronomy Club at Allegheny College for two years. I also co-host and organize Astronomy on Tap, Pittsburgh where we bring the joy of astronomy to the general public. I also enjoy reading, hiking and traveling to new places. 

#### Links

[Works](./works.html)

* * *

## Research

* **Carnegie Mellon University (August 2019 -- present)** - My work involves using novel force calculation techniques like the fast multipole method for the *N*-body problem. Our FMM based code, *Taichi*, has been used to simulate dense stellar systems such as nuclear star clusters and how they affect the mergers of massive black holes. I am primarily working on simulations of sources of low-frequency Gravitational Waves (GW) like massive black hole binaries but have also worked on other projects that include capture of interstellar objects and examining the effect of dark matter spikes on GWs as a method to detect dark matter. 

* **Los Alamos National Lab (May 2018 -- August 2018)** - I was a co-design summer school student where I worked on optimization of an arbitrary Lagrangian Eulerian code called FleCSALE for the triple point problem. Along with my colleagues, I researched MPI+X hybrid programming techniques. Additionally, I used CUDA to port various high order interpolation algorithms used by EOSPAC to GPUs. I also explored the usage of machine learning to replace interpolation calls to EOSPAC. 

* **Leiden University (May 2017 -- August 2018)** - As a LEAPS student, I was researching the secular evolution of the solar system and its debris disk in the birth cluster. I worked with different high order integrators (symplectic and non-symplectic) and investigated coupling of astrophysical codes using Astrophysical Multipurpose Software Environment (AMUSE). 

* * *

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

* * *

## Publications 
1. [_Fast Multipole Methods for N-body Simulations of Collisional Star Systems_ **Mukherjee, D.**, Zhu, Q., Trac, H., Rodriguez, C.L. ApJ 916 9](https://iopscience.iop.org/article/10.3847/1538-4357/ac03b2)
2. [_Evolution of massive black hole binaries in collisionally relaxed nuclear star clusters–Impact of mass segregation_  **Mukherjee, D.**, Zhu, Q., Ogiya, G., Rodriguez, C. L., & Trac, H. Monthly Notices of the Royal Astronomical Society, 518(4), 4801-4817](https://academic.oup.com/mnras/article-abstract/518/4/4801/6840259)
3. [_Close encounters of the interstellar kind: exploring the capture of interstellar objects in near-Earth orbit_  **Mukherjee, D.**, Siraj, A., Trac, H., & Loeb, A.  Monthly Notices of the Royal Astronomical Society, 525(1), 908-921](https://academic.oup.com/mnras/article-abstract/525/1/908/7233732)
4. [_Examining the Effects of Dark Matter Spikes on Eccentric Intermediate Mass Ratio Inspirals Using N-body Simulations_ **Mukherjee, D.**, Holgado, A. M., Ogiya, G., & Trac, H. arXiv preprint arXiv:2312.02275](https://arxiv.org/abs/2312.02275)
5. [_MAGICS I. The First Few Orbits Encode the Fate of Seed Massive Black Hole Pairs_ Chen, N., **Mukherjee, D.**, Di Matteo, T., Ni, Y., Bird, S., & Croft, R.  arXiv preprint arXiv:2312.09183](https://arxiv.org/abs/2312.09183)

## Talks
1. _Optimizing FleCSALE with EOSPAC for Exascale Systems_ Invited talk at **Los Alamos National Lab**. 26 July 2018.
2. _Exploring the Secular Evolution of the Solar System and Debris Disk in the Birth Cluster_ Talk at the **50th DPS meeting, Knoxville.** 23 October 2018.
3. _Fast Multipole Methods for Collisional Systems_ Talk at Hernquist group meeting at **Center for Astrophysics, Harvard University.** April 2021.
4. _Evolution of Massive Black Hole Binaries in Mergers of Collisionally Relaxed Nuclear Star Clusters_ Talk at **Cosmology from Home 2022**. Summer 2022.
5. _Uncovering the Secrets of Galactic Nuclei using Massive Black Hole Binaries_ Invited talk at **Allegheny College**. September 2022.
6. _Evolution of Massive Black Hole Binaries in Mergers of Collisionally Relaxed Nuclear Star Clusters_ Talk at **ChalCA-IV**. November 2022.
7. _Evolution of Massive Black Hole Binaries in Mergers of Collisionally Relaxed Nuclear Star Clusters_ Talk at **Nordic Winter School for Gravitational Wave Astrophysics 2023**. January 2023.
8. _Evolution of Massive Black Hole Binaries in Mergers of Collisionally Relaxed Nuclear Star Clusters_ Talk at **Fifth Neighborhood Workshop on Cosmology at Penn State University**. April 2023.
9. _Exploring Massive Black Hole Binary mergers using Fast Multipole Methods_ Invited talk at **University of Helsinki**. April 2023.
10. _Exploring capture of interstellar objects in Near Earth Orbit_ Invited talk at **Institute for Theory and Computation, Harvard University**. October 2023

## Posters
1. _Heating of Debris Disk using Stellar Encounters._ **April Meeting of the American Physical Society,
Columbus. April 2018.**
2. _Optimizing Next Generation Hydrodynamics Code for Exascale Systems._ **Supercomputing 2018, Dallas. November 2018**


* * *

