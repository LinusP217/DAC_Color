# DAC‒Color Elucidation
[comment]: [![DOI:<10.1021/acs.jpca.4c02927>](http://img.shields.io/badge/JPCA_Paper-10.1021/acs.jpca.4c02927-blue.svg)](http://dx.doi.org/10.1021/acs.jpca.4c02927) 
[comment]: [![ChemRxiv](http://img.shields.io/badge/ChemRxiv-10.26434/chemrxiv--2024--blwjs-EEEA62.svg)](http://dx.doi.org/10.26434/chemrxiv-2024-blwjs)
[comment]: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.11086701.svg)](https://doi.org/10.5281/zenodo.11086701)

<img align="right" src='https://github.com/LinusP217/DAC_Color/blob/main/MO8_LUCO_res.png' width = "200" height = "189">

This repository contains the supporting information for the *Dalton Transactions* submitted manuscript 'Elucidating the direct air capture-induced color change of K<sub>3</sub>[V(O<sub>2</sub>)<sub>4</sub>] with *ab initio* modeling'. All input files needed to reproduce the computational figures are provided herein. Calculations were carried out in the CASTEP 20.11<sup>1</sup> and OptaDOS 1.2.380<sup>2</sup> software packages with different XC functionals and MP k-grid combinations (*vide infra*). Experimental diffuse reflectance spectra were collected at room temperature on a Jasco V-670 spectrophotometer.

## DFT Calculation Parameters

| Calculation       | XC Functional | K<sub>3</sub>[V(O<sub>2</sub>)<sub>4</sub>] | K<sub>3</sub>[VO(O<sub>2</sub>)<sub>2</sub>(CO<sub>3</sub>)] | K[VO<sub>3</sub>]   |
|------------------|---------------|----------|----------------|----------|
| Optimization      | rSCAN         | 3×3×3    | 3×3×3          | 4×2×4    |
| Bandstructure     | PBE           | 3×3×3    | 3×3×3          | 4×2×4    |
| PDOS/isosurfaces  | rSCAN         | 6×6×6    | 6×6×6          | 6×4×6    |
| Absorption        | rSCAN         | 6×6×6    | 6×6×6          | 6×4×6    |


## Contents
```
.
├── computational/
│   │
│   ├── K3VO8/
│   │   ├── PDOS/           # Projected Density of States
│   │   │   ├── K3VO8.cell  # PDOS castep input structure file
│   │   │   └── K3VO8.param # PDOS castep input parameter file
│   │   │
│   │   ├── absorption/     
│   │   │   ├── K3VO8.cell
│   │   │   ├── K3VO8.param
│   │   │   └── K3VO8.odi   # OptaDOS input file (run after castep is finished)
│   │   │
│   │   ├── bandstructure/  # Γ -> X -> P -> N -> Γ -> Z
│   │   │   ├── K3VO8.cell
│   │   │   └── K3VO8.param
│   │   │
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
│   ├── orbital_colours.conf  # color codes for the sumo PDOS plots
│   ├── plotting_commands.md  # bash plotting commands for sumo
│   ├── Color_Calculate.ipynb # Jupyter Notebook with color calc. functions 
│   └── simulated_spectra/    # DFT-derived spectra with various broadening schemes
│       ├── K3VO5CO3_adaptive.txt  # adaptive broadening
│       ├── K3VO5CO3_fixed_01.txt  # fixed width 0.1 eV gaussian broadening
│       ├── K3VO5CO3_fixed_02.txt  #           " 0.2 eV "
│       ├── K3VO5CO3_fixed_03.txt  #           " 0.3 eV "
│       ├── K3VO5CO3_fixed_04.txt  #           " 0.4 eV "
│       ├── K3VO8_adaptive.txt
│       ├── K3VO8_fixed_01.txt
│       ├── K3VO8_fixed_02.txt
│       ├── K3VO8_fixed_03.txt
│       ├── K3VO8_fixed_04.txt
│       ├── KVO3_adaptive.txt
│       ├── KVO3_fixed_01.txt
│       ├── KVO3_fixed_02.txt
│       ├── KVO3_fixed_03.txt
│       └── KVO3_fixed_04.txt
│
├── experimental/    # Experimental data gathered at room temperature with a Jasco V-670
│   ├── K3VO8_abs.csv      # Kubelka-Munk absorbance, A = (1 - R)^2/(2R)
│   ├── K3VO8_reflect.csv  # Diffuse reflectance
│   ├── K3VO4_abs.csv
│   ├── K3VO4_reflect.csv
│   ├── K3VO5CO3_abs.csv
│   ├── K3VO5CO3_reflect.csv
│   ├── KVO3_abs.csv
│   └── KVO3_reflect.csv

18 directories, 56 files

```
## Instructions

Make a copy of the entire repo with the following command in a terminal:
```bash
git clone https://github.com/tjz21/DAC_Color.git
```

or if you would just like a specific file:

<img align="center" src='https://github.com/LinusP217/DAC_Color/blob/main/raw_link_image.png' width = "600" height = "63.4">

```bash
wget [raw URL of specific file]
```

---

GitHub repository maintained by Tim J. Zuehlsdorff, tim.zuehlsdorff@oregonstate.edu

[cc-zero-png]: https://licensebuttons.net/l/zero/1.0/88x31.png "CC0 1.0 Universal (CC0 1.0) Public Domain Dedication button"
[cc-zero]: https://creativecommons.org/publicdomain/zero/1.0/

[![CC0 1.0 Universal (CC0 1.0) Public Domain Dedication
button][cc-zero-png]][cc-zero]
