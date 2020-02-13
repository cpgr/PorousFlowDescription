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
    orcid: 0000-0002-7315-6597
    affiliation: 1
  - name: Jonathan Ennis-King
    orcid: 0000-0002-4016-390X
    affiliation: 1
affiliations:
  - name: CSIRO (Commonwealth Scientific and Industrial Research Organisation)
  - index: 1
date: 13 February 2020
bibliography: paper.bib
---

# Summary

Transport and flow in porous media are important in many practical fields of research.  For instance, the ``PorousFlow`` module that is presented here has been used in the following applications (need refs).

- Groundwater studies [@herron].  This often involves assessing the impacts of human interventions on groundwater resources, and the consequences on the biosphere.  It is frequently necessary to use large and complex models that include the effect of rainfall patterns, spatially and temporally varying evaporation and transpiration, seasonal river flows, realistic topography and hydrogeology, as well as human factors such as mines, water bores, dams, etc.  In certain situations, such as assessing the impact of mining on groundwater, it is vital that the model includes the deformation of the porous material (the rock) since this greatly impacts groundwater flow.  In other situations, it is useful to be able to track the transport of tracers and pollutants through the system.  In other situations, it is necessary to model the unsaturated (vadose) zone, where air and groundwater coexist in the subsurface.

- Geothermal modelling: the simulation of natural and man-made geothermal systems, typically in order to quantify heat energies that may be extracted.  Models in this field involve the coupled transport of heat and fluid.  Many models are often large-scale, but some focus on small regions close to wellbores to investigate wellbore integrity.  In this field, it often is useful to assess the impacts of subsurface heterogeneity, realistic pumping regimes, geochemical effects, fracture flow, and the creation of new fractures through deliberate or unintentional hydrofracturing, as well as potential microseismicity.

- Multiphase modelling, such as the simulation of CO$_{2}$ sequestration, H$_{2}$ storage, or methane flows around coal mines.  These simulations involve the interaction and flow of at least two fluid phases (e.g. gas and water).  Changes in temperature often impact these flows, and realistic equations of state for the fluids involved are necessary.  For instance, CO$_{2}$ sequestration typically involves pumping high-pressure, cold CO$_{2}$ into a warmer aquifer filled with brine: the CO$_{2}$ heats and dissolves into the brine, changing its density and flow characteristics.  In many of these models, the altered pressure and temperature can potentially cause mechanical failure of the subsurface, and hence the creation of new flow paths and microseismicity.

Other situations where porous-flow physics is used include oil and gas production, nuclear waste repositories and chemical leaching.

In many of these examples it is not enough to simply solve simplistic, traditional flow and transport physics.  Coupling with other physics is necessary: solid mechanical deformations and stresses can be important; geochemistry can alter the flow characteristics of the subsurface; high-precision equations of state are required; the evolution of fluid components (tracers, pollutants, reactants) is of interest; unsaturated physics is crucial.  The flow and transport often impacts the subsurface structure, and conversely, the effects of these structure-changes impact the flow and transport.

Simulating these situations can be challenging in practice.  Many existing simulation codes that are widely used focus on only a subset of physical processes, and therefore accurate modelling often requires the use of several loosely-coupled software packages.  Such an approach can be useful in many problems of interest, particularly where the characteristic time scales for each physical process are sufficiently different.  In other instances, however, the ability to tightly couple different physical processes is necessary due to comparable characteristic time scales for the different physical processes.
``PorousFlow`` module of allows simulation of all the relevant thermal-hydraulic-mechanical-chemical physical phenomenon in a tightly-coupled framework.

``PorousFlow`` is built upon the open-source, massively parallel, fully implicity multiphysics simulation framework called MOOSE (the Multiphysics Object-Oriented Simulation Environment) [@permann2019moose]  MOOSE is an open-source library from the Idaho National Laboratory that provides a high-level interface to the libMesh finite element library [@libmesh] and PETSc nonlinear
solvers [@petsc].

For convenience, the source code for ``PorousFlow``, https://github.com/idaholab/moose/tree/master/modules/porous_flow, is bundled within the MOOSE framework, https://github.com/idaholab/moose, and detailed documentation found at https://mooseframework.org/modules/porous_flow/index.html.

# References
