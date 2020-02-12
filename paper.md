---
title: 'PorousFlow: a multiphysics simulation code for coupled problems in porous media'
tags:
  - C++
  - porous flow
  - multiphysics
  - THMC
  - Darcy flow
authors:
  - name: Andy Wilkins
    orcid: 0000-0001-6472-9560
    affiliation: 1
  - name: Christopher P. Green
    orcid: 0000-0001-6472-9560
    affiliation: 1
  - name: Jonathan Ennis-King
    orcid: 0000-0001-6472-9560
    affiliation: 1
affiliations:
  - name: CSIRO (Commonwealth Scientific and Industrial Research Organisation)
  - index: 1
date: 13 February 2020
bibliography: paper.bib
---

# Summary

Transport and flow in porous media are important in many practical fields of research.  For instance, the ``PorousFlow`` module that is presented here has been used in the following applications (need refs).

- Groundwater studies.  This often involves assessing the impacts of human interventions on groundwater resources, and the consequences on the biosphere.  Frequently, it is necessary to use large and complex models that include the effect of rainfall patterns, spatially and temporally varying evaporation and transpiration, seasonal river flows, realistic topography and hydrogeology, as well as human factors such as mines, water bores, dams, etc.  In certain situations, such as assessing the impact of mining on groundwater, it is vital that the model includes the deformation of the porous material (the rock) since this greatly impacts groundwater flow.  In other situations, it is useful to be able to track the transport of tracers and pollutants through the system.

- Geothermal modelling: the simulation of natural and man-made geothermal systems, typically in order to quantify potential heat energies.  Models in this field involve the coupled transport of heat and fluid.  Many models are often large-scale, but some focus small regions close to wellbores to investigate wellbore integrity.  Increasingly, it is useful to assess the impacts of subsurface heterogeneity, realistic pumping regimes, geochemical effects, fracture flow, and the creation of new fractures through deliberate or unintentional hydrofracturing, as well as potential microseismicity.

- Multiphase modelling, such as the simulation of CO$_{2}$ sequestration, H$_{2}$ storage, or methane flows around coal mines.  These simulations involve the interaction and flow of at least two fluid phases (gas and water).  Often, changes in temperature impacts these flows, and realistic equations of state for the fluids involved are necessary.  For instance, CO$_{2}$ sequestration typically involves pumping high-pressure, cold CO$_{2}$ into a warmer aquifer filled with brine.  The CO$_{2}$ heats and dissolves into the brine, causing changes in its density and flow characteristics.  The enhanced pressure and altered temperature can cause mechanical failure of the aquifer, and hence the creation of new flow paths and potential microseismicity.

In many of these examples it is not enough to simply solve simplistic, traditional flow and transport physics.  Coupling with other physics is necessary: solid mechanical deformations and stresses can be important; geochemistry can alter the flow characteristics of the porous material; high-precision equations of state are required; the evolution of fluid components (tracers, pollutants, reactants) is of interest.  The flow and transport often impacts the subsurface structure, and conversely, the effects of these structure changes impact the flow and transport.

The ``PorousFlow`` module of the open-source, multiphysics simulation framework called ``MOOSE`` allows simulation of all these physical phenomenon.

The forces on stars, galaxies, and dark matter under external gravitational
fields lead to the dynamical evolution of structures in the universe. The orbits
of these bodies are therefore key to understanding the formation, history, and
future state of galaxies. The field of "galactic dynamics," which aims to model
the gravitating components of galaxies to study their structure and evolution,
is now well-established, commonly taught, and frequently used in astronomy.
Aside from toy problems and demonstrations, the majority of problems require
efficient numerical tools, many of which require the same base code (e.g., for
performing numerical orbit integration).

``Gala`` is an Astropy-affiliated Python package for galactic dynamics. Python
enables wrapping low-level languages (e.g., C) for speed without losing
flexibility or ease-of-use in the user-interface. The API for ``Gala`` was
designed to provide a class-based and user-friendly interface to fast (C or
Cython-optimized) implementations of common operations such as gravitational
potential and force evaluation, orbit integration, dynamical transformations,
and chaos indicators for nonlinear dynamics. ``Gala`` also relies heavily on and
interfaces well with the implementations of physical units and astronomical
coordinate systems in the ``Astropy`` package [@astropy] (``astropy.units`` and
``astropy.coordinates``).

``Gala`` was designed to be used by both astronomical researchers and by
students in courses on gravitational dynamics or astronomy. It has already been
used in a number of scientific publications [@Pearson:2017] and has also been
used in graduate courses on Galactic dynamics to, e.g., provide interactive
visualizations of textbook material [@Binney:2008]. The combination of speed,
design, and support for Astropy functionality in ``Gala`` will enable exciting
scientific explorations of forthcoming data releases from the *Gaia* mission
[@gaia] by students and experts alike. The source code for ``Gala`` has been
archived to Zenodo with the linked DOI: [@zenodo]

# Acknowledgements

We acknowledge contributions from Brigitta Sipocz, Syrtis Major, and Semyeong
Oh, and support from Kathryn Johnston during the genesis of this project.

# References
