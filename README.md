# Direct Air Capture
[comment]: [![DOI:<10.1021/acs.jpca.4c02927>](http://img.shields.io/badge/JPCA_Paper-10.1021/acs.jpca.4c02927-blue.svg)](http://dx.doi.org/10.1021/acs.jpca.4c02927) 
[comment]: [![ChemRxiv](http://img.shields.io/badge/ChemRxiv-10.26434/chemrxiv--2024--blwjs-EEEA62.svg)](http://dx.doi.org/10.26434/chemrxiv-2024-blwjs)
[comment]: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.11086701.svg)](https://doi.org/10.5281/zenodo.11086701)

<img align="right" src='https://github.com/tjz21/DAC_metals/blob/main/MO8_structure.png' width = "189" height = "200">

This repository contains the computational supporting information for the [*JPC A* publication](https://doi.org/10.1021/acs.jpca.4c02927), 'Electronic Structure and CO<sub>2</sub> Reactivity of Group IV/V/VI Tetraperoxometalates'. All parameters and structures needed to reproduce the reaction mechanism for [M(O<sub>2</sub>)<sub>4</sub>]<sup>x-</sup> + CO<sub>2</sub> &rarr; [MO(O<sub>2</sub>)<sub>2</sub>CO<sub>3</sub>]<sup>x-</sup> + O<sub>2</sub> are contained herein. Geometry optimizations were carried out in the Gaussian 16 Rev A.03<sup>1</sup> software package with the CAM-B3LYP functional. LANL2DZ was used for the metal center while C and O were modelled with 6-31+G\*. All xyz structures contain the 298.15 K Gibbs free energy in Ha in the comment line. Calculation summaries in each directory were produced using ESIgen.<sup>2</sup>

## Contents
```
.
├── computational/
│   │
│   ├── K3VO8/
│   │   ├── PDOS/           # Projected Density of States
│   │   │   ├── K3VO8.cell  # castep input structure file
│   │   │   └── K3VO8.param # castep input parameter file
│   │   ├── absorption/     
│   │   │   ├── K3VO8.cell
│   │   │   ├── K3VO8.odi   # OptaDOS input file (run after castep is finished)
│   │   │   └── K3VO8.param
│   │   ├── bandstructure/  # Γ -> X -> P -> N -> Γ -> Z
│   │   │   ├── K3VO8.cell
│   │   │   └── K3VO8.param
│   │   └── optimization/
│   │       ├── K3VO8.cell
│   │       └── K3VO8.param
│   │
│   ├── K3VO5CO3/
│   │   ├── PDOS/
│   │   ├── absorption/
│   │   ├── bandstructure/ # Γ -> Y -> V -> Γ -> A -> M -> L -> V
│   │   └── optimization/
│   │
│   ├── KVO3/
│   │   ├── PDOS/
│   │   ├── absorption/
│   │   ├── bandstructure/ # Γ -> Y -> V -> Γ -> A -> M -> L -> V
│   │   └── optimization/
│   │
│   ├── orbital_colours.conf
│   └── plotting_commands.md
│
├── experimental/    # Data gathered at room temperature with a Jasco V-670
│   ├── K3VO8_abs.csv      # Kubelka-Munk absorbance
│   ├── K3VO8_reflect.csv  # Diffuse reflectance
│   ├── K3VO4_abs.csv
│   ├── K3VO4_reflect.csv
│   ├── K3VO5CO3_abs.csv
│   ├── K3VO5CO3_reflect.csv
│   ├── KVO3_abs.csv
│   └── KVO3_reflect.csv

NUM directories, NUM files

```
## Instructions

Make a copy of the entire repo with the following command in a terminal:
```bash
git clone https://github.com/tjz21/DAC_Color.git
```

or if you would just like a specific file:

<img align="center" src='https://github.com/tjz21/CO2_SFG_DFT/blob/main/raw_link_image.png' width = "600" height = "63.4">

```bash
wget [raw URL of specific file]
```

---
GitHub repository maintained by Tim J. Zuehlsdorff, tim.zuehlsdorff@oregonstate.edu


