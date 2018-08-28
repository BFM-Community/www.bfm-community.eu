---
layout: page
title:  Description
id: bfm-description
description: |
---

## BFM background and modelling framework

The ***Biogeochemical Flux Model (BFM)*** is a numerical model, which
describes the dynamics of major biogeochemical processes occurring in
marine systems. Presently BFM considers the cycles of nitrogen,
phosphorus, silica, carbon, and oxygen in the water dissolved phase,
as well as in the plankton, detritus, and benthic compartments.
Plankton dynamics are parameterized by considering a number of
plankton functional groups, each representing a class of taxa. BFM
plankton functional groups are subdivided in producers
(phytoplankton), consumers (zooplankton), and decomposers (bacteria).
These broad functional classifications are further partitioned into
functional subgroups to create a planktonic food web (e.g. diatoms,
picophytoplankton, microzooplankton,
etc.).

The BFM code can be easily coupled to standard hydrodynamics codes,
allowing for explicit description of the dynamics of biogeochemical
properties in a spatially heterogeneous system. Presently BFM has been
successfully coupled to the Princeton Ocean Model (POM), the Ocean
Parallelise’ (OPA), and Nucleus for European Modelling of the Ocean
(NEMO) and applied at the global ocean, regional, subregional and
local space scales. When coupled with the hydrodynamics BFM can be
used as a short term forecasting model or as a climate simulation
model.

From a mathematical point of view, the BFM is a set of ordinary
differential equations describing the time rate of change of a number
of biogeochemically active tracers. The BFM structure is flexible and
modular, so that the number, type and properties of the functional
groups can be easily modified and different model configurations can
be used to focus on different aspects. The code is written in the
FORTRAN90 language.

In the future also some of the coupled physical-BFM systems will be
released as examples of the complete modelling suite to be used for
the simulation of the marine ecosystem dynamics.

<img class="center-me" src="{{site.baseurl}}/img/bfm_scheme_V5_pelagic_web.png" width="65%">
