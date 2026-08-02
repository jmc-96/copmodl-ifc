# CoPModL-IFC

> **Towards an IFC-Based Construction Process Modeling Language**

CoPModL-IFC is a domain-specific modeling language (DSML) that integrates the
product and spatial semantics of the
[Industry Foundation Classes (IFC)](https://www.buildingsmart.org/standards/bsi-standards/industry-foundation-classes/)
with construction-process concepts from the Construction Process Modeling Language [(CoPModL)](https://www.sciencedirect.com/science/article/pii/S0306437919305095). 
The language is implemented on the [ADOxx](https://www.adoxx.org/) metamodeling platform and combines IFC-based building structures with process tasks and behavioral constraints.

## Repository contents

| Path | Description |
| --- | --- |
| `adoxx/CoPModL-IFC Library v0.0.1.abl` | ADOxx library defining the current CoPModL-IFC DSML. |
| `adoxx/models v0.0.1.adl` | ADOxx model file (ADL export) containing the case-study models built with the CoPModL-IFC library. |
| `dataset/Building-Architecture.ifc` | Reference BIM model obtained from the buildingSMART International Sample-Test-Files repository. |
| `dataset/Building-Architecture_modified.ifc` | Modified case-study model containing renamed objects, additional property sets, and `IfcTask` instances representing construction interventions. |
| `3d-objects/Outer_wall - North.ply` | Geometry of the outer north wall extracted from the reference BIM model using [Bonsai](https://bonsaibim.org/). |
| `README.md` | Overview of the project, research, release, and citation information. |
| `LICENSE` | License applicable to the original project materials, subject to the third-party terms described below. |

## Getting started

1. Download the required version from the Releases page or clone the repository.
2. Open an ADOxx development environment.
3. Import `adoxx/CoPModL-IFC Library v0.0.1.abl` using the ADOxx library-management functionality.
4. Create or open models in `adoxx/models v0.0.1.adl` using the ADOxx ADL import tool.
5. Use the files in `dataset/` to inspect or reproduce the case-study scenario in BIM environments.

## Project status

The current documented release is **CoPModL-IFC v0.0.1**. This release represents the ADOxx implementation and case-study associated with the BPMDS/EMMSAD 2026 paper, together with documentation and metadata corrections. CoPModL-IFC remains an active research project.

The implemented approach demonstrates how IFC product and spatial structures
can be integrated with construction-process tasks and behavioral constraints
at the metamodel level.

Ongoing work and proposed extensions include:

- extending the conceptual mapping between IFC and CoPModL elements;
- refining the representation of behavioral constraints in BIM-oriented contexts;
- improving the ADOxx-based implementation of the integration approach;
- expanding validation through additional datasets and modeling scenarios;
- consolidating the integration of `IfcFurnishingElement` and its subtype `IfcFurniture`;
- improving validation and reproducibility of the experiments.

## Data provenance and third-party materials

`dataset/Building-Architecture.ifc` originates from the
[buildingSMART International Sample-Test-Files repository](https://github.com/buildingSMART/Sample-Test-Files). The buildingSMART sample files are provided under the
[Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).
The corresponding attribution requirements continue to apply to the source
dataset and derived artifacts.

`dataset/Building-Architecture_modified.ifc` is a modified derivative used for
the paper's case study. Its modifications include renamed objects, additional
property sets, and construction interventions represented using `IfcTask` instances. The PLY object under `3d-objects/` was modeled as part of the sample IFC file extensions.

## Citation

When using the concepts, implementation, or experimental artifacts from this
repository, please cite the accompanying conference paper:

```bibtex
@inproceedings{munozcadiz2026copmodlifc,
  author    = {Mu{\\~n}oz-C{\\'a}diz, Jes{\\'u}s and Challa, Gunakar and Curty, Simon and Fill, Hans-Georg},
  editor    = {van der Aa, Han and Guizzardi, Renata and Hacks, Simon and Pufahl, Luise},
  title     = {Towards an {IFC}-Based Construction Process Modeling Language},
  booktitle = {Enterprise, Business-Process and Information Systems Modeling},
  series    = {Lecture Notes in Business Information Processing},
  volume    = {594},
  pages     = {431--448},
  year      = {2026},
  publisher = {Springer},
  address   = {Cham},
  doi       = {10.1007/978-3-032-28274-3_27},
  url       = {https://doi.org/10.1007/978-3-032-28274-3_27}
}
```

## Acknowledgments

This work was supported by the
[Smart Living Lab](https://www.smartlivinglab.ch/en/), funded by the University
of Fribourg, EPFL, and HEIA-FR.