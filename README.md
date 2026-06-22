# CoPModL-IFC

> **Towards an IFC-based Construction Process Modeling Language**

A conceptual integration that maps the product-modeling semantics of the
Industry Foundation Classes (IFC) onto the Construction Process Modeling
Language (CoPModL), implemented as a domain-specific modeling language (DSML)
on the [ADOxx](https://www.adoxx.org/) meta-modeling platform.

This repository accompanies the paper *"Towards an IFC-Based Construction
Process Modeling Language"* (Muñoz-Cádiz, Challa, Curty & Fill), published in
the **BPMDS/EMMSAD 2026** proceedings (LNBIP vol. 594, Springer) —
[doi:10.1007/978-3-032-28274-3_27](https://doi.org/10.1007/978-3-032-28274-3_27).
It contains the ADOxx library, the datasets, and the supporting artifacts used to
develop and evaluate the approach.

---

## Case study

The approach is evaluated on an official
[buildingSMART International sample test file](https://github.com/buildingSMART/Sample-Test-Files)
— a partially modeled single-storey residential house. The metadata was extended
to define an intervention scenario: constructing the missing outer north wall and
an attached column that bound the living-room area.

From this enriched model, both a **configuration** model (mapped IFC spatial
hierarchy) and a **flow** model (the 4D intervention plan) were built in ADOxx.

## Repository contents

| Path | Description |
| --- | --- |
| `CoPModL_IFC.abl` | ADOxx library (`.abl`) defining the CoPModL-IFC DSML. Import it into ADOxx to obtain the Flow and IFC Product Hierarchy model-types. |
| `dataset/Building-Architecture.ifc` | Original reference dataset from buildingSMART International. |
| `dataset/Building-Architecture_modified.ifc` | Adapted version used for the case-study scenario (renamed objects, added property sets and `IfcTask` interventions). |
| `3d-objects/Outer_wall - North.ply` | Outer north wall object extracted from the reference project using [Bonsai BIM](https://bonsaibim.org/). |
| `library-models/` | Example ADOxx models built on the CoPModL-IFC library *(in progress)*. |
| `LICENSE` | MIT license. |

## Project status

This is an **ongoing research project**. The conceptual design, the ADOxx
implementation, and the dataset-based experiments are actively evolving. Current
results are encouraging, but the framework remains under refinement.

Work in progress includes:

- extending the conceptual mapping between IFC and CoPModL elements;
- refining the representation of behavioral constraints in BIM-oriented contexts;
- improving the ADOxx-based implementation of the integration approach;
- expanding validation through additional datasets and modeling scenarios;
- consolidating the integration of `IfcFurnishingElement` and its subtype
  `IfcFurniture`;
- improving documentation and reproducibility of the experiments.

## Citation

If you use this work, please cite the accompanying paper:

```bibtex
@inproceedings{munozcadiz2026copmodlifc,
  author    = {Mu\~{n}oz-C\'{a}diz, Jes\'{u}s and Challa, Gunakar and Curty, Simon and Fill, Hans-Georg},
  editor    = {van der Aa, Han and Guizzardi, Renata and Hacks, Simon and Pufahl, Luise},
  title     = {Towards an {IFC}-Based Construction Process Modeling Language},
  booktitle = {Enterprise, Business-Process and Information Systems Modeling (BPMDS 2026, EMMSAD 2026)},
  series    = {Lecture Notes in Business Information Processing},
  volume    = {594},
  year      = {2026},
  publisher = {Springer},
  address   = {Cham},
  doi       = {10.1007/978-3-032-28274-3_27}
}
```

## Authors

Jesús Muñoz-Cádiz, Gunakar Challa, Simon Curty, and Hans-Georg Fill —
Research Group Digitalization and Information Systems, University of Fribourg,
Switzerland.

## Acknowledgments

This work was supported by the
[Smart Living Lab](https://www.smartlivinglab.ch/en/), funded by the University
of Fribourg, EPFL, and HEIA-FR.

## License

Released under the MIT License. See [`LICENSE`](LICENSE) for details.
