---
layout: default
---

## About me

I am a computational astrophysicist purusing my Ph.D. in Physics at Carnegie Mellon University. I obtained my Bachelor of Science in Physics from Allegheny College in 2019.

I have worked in a variety of projects at various scales - solar system dynamics, stellar dynamics in young massive clusters and combining hydrodynamics with gravitational dyanmics for clusters. I am also interested in pursuing topics in cosmology and intermediate mass black hole formation.

I specialize in gravitational dynamics and Smoothed Particle Hydrodynamics. I am currently working on my own code that combines gravitational dynamics and SPH to treat interactions of stars in clusters. I am proficient in Fortran (77,90), C, Python and CUDA.  

On the computer science side of things, I am interested in High Performance Computing, GPU computing, and machine learning.

**You can find my current CV** [here](/docs/CV_github.pdf).

Outside of academics, I am involved in astrophotography. I was the president of the Astronomy Club at Allegheny College for two years. I also enjoy reading, hiking and traveling to new places.

* * *

## Experience

* **Los Alamos National Lab (May 2018 -- August 2018)** - Optimization of an Arbitrary Lagrangian Eulerian code called FleCSALE for the triple point problem. Researched MPI+X hybrid programming techniques. Used CUDA to port various high order interpolation algorithms used by EOSPAC to GPUs. Explored the usage of machine learning to replace interpolation calls to EOSPAC. Presented a poster at Supercomputing 2018 and a talk at CCS division of LANL.

* **Leiden University (May 2017 -- present)** - Exploring the secular evolution of the solar system and its debris disk in the birth cluster. Worked with different high order integrators (symplectic and non-symplectic) and investigated coupling of astrophysical codes using Astrophysical Multipurpose Software Environment (AMUSE). Presented a poster at APS April, 2018 and a talk at DPS 2018. A paper is being written.

* * *

## Current Projects

### Evolution of Primordial Solar System

Using two coupled astrophysical codes, _rebound_ and _NBODY6++_, my collaborators at Leiden University and I are exploring the effects of the Sun's birth cluster on the dynamics of the giant planets and the secular evolution of the debris disk surrounding the planets. 

### PyStarsmasher

Creating a new Python based interface for SPH code _Starsmasher_ which is used for studying stellar mergers. The new interface/code, named _PyStarsmasher_, can be coupled with any other astrophysical code using the Python interface. One can imagine coupling it to gas dynamics or gravitational dynamics codes using AMUSE. _PyStarsmasher_ is an open-source code and can be downloaded [here](https://github.com/dipto4/PyStarsmasher).

### Formation of Runaway Collision Objects

Using _PyStarsmasher_, a novel method has been devised to treat stellar collisions in _NBODY6++_ using _Starsmasher_. This method of coupling codes has not been used before and provides better results while treating stellar mergers in star clusters. This coupled code is then used to study the formation of runaway collision objects in star clusters. 

### NBODY6++

For my bachelor's thesis, I had to work with _NBODY6++_. I worked in modifying the original code to allow for collisions to take place even when stellar evolution is switched off. In addition to that, the new code outputs details of all stars in the cluster for multiple timesteps before a collision has taken place so that it can be tracked. These files can be read using _PyStarsmasher_ to set up a sequence of collisions. The modified code can be found
[here](https://github.com/dipto4/NBODY6_collision_detection).

* * *

## Talks
1. _Optimizing FleCSALE with EOSPAC for Exascale Systems._ Invited talk at **Los Alamos National Lab**. 26 July 2018.
2. _Exploring the Secular Evolution of the Solar System and Debris Disk in the Birth Cluster._ Talk at the **50th DPS meeting, Knoxville.** 23 October 2018.

## Posters
1. _Heating of Debris Disk using Stellar Encounters._ **April Meeting of the American Physical Society,
Columbus. April 2018.**
2. _Optimizing Next Generation Hydrodynamics Code for Exascale Systems._ **Supercomputing 2018, Dallas. November 2018**


* * *

