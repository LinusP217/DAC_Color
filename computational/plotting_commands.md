# 

## Colour Calculations

## *sumo* Plotting Commands
Once *sumo* has been installed (https://github.com/SMTG-Bham/sumo), executing the below commands will generate the figures used in the manuscript.

### Bandstructure
#### 1--K<sub>3</sub>[V(O<sub>2</sub>)<sub>4</sub>]
```
sumo-bandplot --code castep -f seedname.bands --scissor 1.62 --band-edges --format svg --title K3VO8 --ymin -6.0 --ymax +6.0
```
#### 2--K<sub>3</sub>[VO(O<sub>2</sub>)<sub>2</sub>(CO<sub>3</sub>)]
```
sumo-bandplot --code castep -f seedname.bands --scissor 2.85 --band-edges --format svg --title K3VO5CO3 --ymin -6.0 --ymax +6.0
```
#### 3--K[VO<sub>3</sub>]
```
sumo-bandplot --code castep -f seedname.bands --scissor 3.57 --band-edges --format svg --title KVO3 --ymin -6.0 --ymax +6.0
```

### PDOS
#### Atom-Decomposed
```
sumo-dosplot --code castep -f seedname.bands -g 0.1 --config orbital_colours.conf --legend-cutoff 5 --legend-frame --columns 1 --format svg --xmin -6.0 --xmax +6.0
```
#### V(3d) Angular Momentum
```
sumo-dosplot --code castep -f seedname.bands -g 0.1 --orbitals V.d --config orbital_colours.conf --legend-cutoff 5 --legend-frame --columns 1 --format svg --xmin -0.8 --xmax +5.0
```
