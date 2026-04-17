# CoPModL -IFC

Conceptual integration of the Construction Process Modeling Language (CoPModL) and the Industry Foundation Classes (IFC) for BIM-oriented process and data modeling.

## Overview

This repository presents an ongoing research project focused on the conceptual integration of IFC-based product modeling and CoPModL-based process modeling. The work aims to connect standardized BIM data structures with behavior-oriented construction process models in a coherent and implementable way.

The project is developed on the ADOxx meta-modeling platform and places particular emphasis on behavioral constraints in CoPModL, which remain a persistent challenge in BIM-oriented modeling environments.

The applicability of the proposed approach is evaluated using an official dataset from buildingSMART International.

## Repository Contents

- `CoPModL_IFC.abl` — ADOxx library definition for the CoPModL-IFC integration
- `dataset/` — IFC datasets used for testing and validation
  - `Building-Architecture.ifc` — original reference dataset from buildingSMART International
  - `Building-Architecture_modified.ifc` — adapted version for experimentation
- `3d-objects/` — 3D object exports generated from BIM tools
  - `Outer_wall - North.ply` — wall object extracted from the reference project using Bonsai BIM
- `library-models/` — ADOxx model examples based on the CoPModL-IFC library *(in progress)*
- `LICENSE` — licensing information

## Current Status

This is an ongoing research project.

The repository contains evolving artifacts related to conceptual design, implementation, and dataset-based experimentation. Current results are encouraging, but the framework remains under active development and refinement.

## Ongoing Improvements

The following activities are currently in progress:

- extending the conceptual mapping between IFC and CoPModL elements
- refining the representation of behavioral constraints in BIM-oriented contexts
- improving the ADOxx-based implementation of the integration approach
- expanding validation through additional datasets and modeling scenarios
- improving documentation and reproducibility of experiments
- further consolidating the integration of *IfcFurnishingElement* and its subtype *IfcFurniture*

## License

See the `LICENSE` file for licensing information.