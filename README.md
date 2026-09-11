# Parametric CAD Modelling & Additive Manufacturing of Nose Pliers

A mechanical design project focused on developing a **multi-component nose-plier mechanism** from parametric CAD models to a 3D-printable assembly. The project combines component-level modelling, assembly design, STL export, print preparation, and FDM additive manufacturing.

## Project Overview

This project was developed as a hands-on **Mechanical Engineering CAD and Additive Manufacturing** exercise.

The workflow followed:

**Mechanical concept → Parametric CAD modelling → Component assembly → STL export → Slicing/print preparation → 3D-printed parts → Physical assembly**

The final design consists of separate plier components, a pivot pin, and a pivot pin cap that together form the complete nose-plier mechanism.

## Objectives

- Develop detailed mechanical components using **parametric, feature-based CAD modelling**.
- Create a complete assembly with appropriate component interfaces around a pivot.
- Convert CAD geometry into STL files suitable for additive manufacturing.
- Prepare the parts for FDM printing using a slicer and evaluate material usage and print time.
- Translate the digital CAD design into a physical prototype.

## CAD Design

The components were modelled in **Siemens NX** using feature-based modelling techniques.

### Main modelling operations

The part files make use of common mechanical CAD operations such as:

- Constrained sketches
- Extrusions
- Sweeps / revolved features
- Blends / fillets
- Holes
- Pattern features
- Datum/reference geometry

The design was split into separate components so that the plier mechanism could be assembled and manufactured as individual printable parts.

### Components

The project contains the following primary CAD/manufacturing files:

| Component | CAD | STL |
|---|---|---|
| Plier component 1 | `Plier_1.prt` | `Plier_1.stl` |
| Plier component 2 | `Plier_2.prt` | `Plier_2.stl` |
| Pivot pin | `Pivot pin.prt` | `Pivot pin.stl` |
| Pivot pin cap | `Pivot pin cap.prt` | `Pivot pin cap.stl` |
| Complete assembly | `plier assembly.prt` | — |

## Assembly Design

The two plier components are connected through a **pivot-based interface**, allowing the jaws/handles to move relative to one another.

The assembly stage was used to:

- Bring the individual parts into a common mechanical configuration.
- Align the mating components around the pivot.
- Verify the overall fit of the components.
- Prepare the final design for physical fabrication.

The assembly is included as:

```text
plier assembly.prt
```

## Additive Manufacturing

After completing the CAD models, the printable components were exported as **STL** files and prepared in **Bambu Studio**.

The included 3MF project contains **4 printable objects**:

1. `model1.stl`
2. `model2 (Copy of model1).stl`
3. `model3.stl`
4. `Pivot pin cap.stl`

The print setup uses a **0.4 mm nozzle** and **0.20 mm layer height**.

### Key print settings

| Parameter | Value |
|---|---:|
| Filament | PLA |
| Nozzle diameter | 0.4 mm |
| Layer height | 0.20 mm |
| Wall loops | 2 |
| Infill density | 15% |
| Infill pattern | Grid |
| Top shell layers | 5 |
| Bottom shell layers | 3 |
| Brim width | 5 mm |
| Bed | Textured PEI |
| Nozzle temperature | 220 °C |
| Bed temperature | 55 °C |

The slicer project also enables automatic/tree support for the larger plier components where required.

## Print Resource Estimate

The slicing result provides the following estimates for the complete plate:

| Metric | Value |
|---|---:|
| Model filament | 8.08 m |
| Model mass | 24.11 g |
| Support filament | 0.80 m |
| Support mass | 2.40 g |
| **Total filament** | **8.89 m** |
| **Total mass** | **26.51 g** |
| Preparation time | 8 min 19 s |
| Model printing time | 58 min |
| **Total estimated time** | **~1 h 6 min** |
| Estimated cost | 0.53 |

These values are taken from the Bambu Studio slicing configuration/result included with the project.

## Repository Structure

A suggested GitHub repository layout is:

```text
nose-plier-cad-3d-printing/
│
├── README.md
│
├── CAD/
│   ├── Plier_1.prt
│   ├── Plier_2.prt
│   ├── Pivot pin.prt
│   ├── Pivot pin cap.prt
│   └── plier assembly.prt
│
├── STL/
│   ├── Plier_1.stl
│   ├── Plier_2.stl
│   ├── Pivot pin.stl
│   └── Pivot pin cap.stl
│
├── Slicer/
│   └── BambuStudio.3mf
│
└── Images/
    ├── cad-model.png
    ├── assembly.png
    ├── slicing-result.png
    └── printed-assembly.png
```

> Rename the 3MF file to something cleaner such as `BambuStudio.3mf` when organizing the GitHub repository.

## Tools & Technologies

- **Siemens NX** — Parametric 3D CAD modelling and assembly
- **Bambu Studio** — Slicing and FDM print preparation
- **STL** — Additive manufacturing geometry format
- **FDM 3D Printing** — Physical prototyping

## Engineering Workflow

### 1. Component Modelling
Individual plier and pivot components were created as parametric solid models.

### 2. Assembly
The components were brought together into a complete pivot-based nose-plier assembly.

### 3. Manufacturing Export
Printable components were exported from CAD as STL files.

### 4. Slicer Preparation
The STL files were arranged on the build plate and configured for FDM printing, including layer height, infill, wall count, brim and supports.

### 5. Physical Prototyping
The generated toolpaths were used to fabricate the components as a physical prototype, allowing the digital design to be translated into a functional mechanical assembly.

## Engineering Takeaways

This project provided practical experience in:

- Parametric mechanical CAD
- Feature-based solid modelling
- Mechanical assembly
- Component interfacing
- Design for additive manufacturing
- STL preparation
- FDM print parameter selection
- Rapid physical prototyping

## Notes

The repository represents the project as a **CAD-to-prototype workflow**. It focuses on mechanical modelling, assembly and fabrication rather than numerical structural analysis or force/tolerance validation.

No claims of FEA, strength optimization, dimensional tolerance analysis, or quantified mechanical performance are made unless separately documented.

## Project Summary

**Designed → Modelled → Assembled → Exported → Sliced → 3D Printed**

The project demonstrates how a mechanical product can be developed from a digital parametric CAD model into a physical prototype using modern additive manufacturing.

---

## Suggested GitHub Description

> **Parametric nose-plier designed in Siemens NX and converted into a 3D-printable assembly using STL export and Bambu Studio, covering CAD modelling, assembly and FDM additive manufacturing.**
