# blastfoam

_blastFoam_ is a solver for multi-component compressible flow with application to high-explosive detonation, explosive safety and air blast. 



Math: <img alt="$ \frac{1}{2} $" src="svgs/4f0f90de9798f24da0a8a43f21b62ad2.png" align="middle" width="6.552644999999998pt" height="27.775769999999994pt"/>





## Get the code

blastFoam is free. blastFoam is currently in pre-release beta. If you'd like to request a copy of the code and solver before the official public release, while we're in beta, just get in touch: blastfoam@synthetik-technologies.com


## Features

_blastFoam_ currently supports the following features:

- An arbitrary number of phases/EOS's
- JLW equation of state with constant, linear, and "Miller" afterburn models
- Multiple example and tutorial cases
- Automatic mesh refinement (AMR)
- Single and multi-point detonation
- High-order (1st, 2nd, and 4th order in time; 3rd order spatial)
- HLLC, AUSM+, Kurganov, Tadmor flux schemes
- Parallel (MPI)
- Compatible with all standard OpenFOAM mesh generation, pre- and post-processing utilities



## Equations of State

blastFoam includes the following equations of state:

- Jones Wilkens Lee (with afterburn)
- Ideal Gas
- Stiffened Perfect Gas
- Cochran-Chan
- Tait



## Verification and Validation

_blastFoam_ has been validated against known solutions to standard gas dynamics problems, and against data from physical tests.  






## Governing Equations


The evolution of a two phase, compressible, and inviscid mixture can be defined by a set of coupled evolution equations for mass, momentum, and energy. 

<p align="center"><img alt="$$&#10;    \partial_t \mathbf{U} + \nabla \cdot \mathbf{F} = \mathbf{S}&#10;$$" src="svgs/10b5fb69900ce3e0ba80d06da2efff49.png" align="middle" width="119.034795pt" height="13.881251999999998pt"/></p>

<p align="center"><img alt="$$&#10;    \mathbf{U} = &#10;        \left( \begin{array}{c}&#10;           \alpha_1 \\&#10;           \alpha_1 \rho_1 \\&#10;           \alpha_2 \rho2 \\&#10;           \rho \mathbf{u} \\&#10;           \rho E&#10;        \end{array} \right)&#10;    \mathbf{F} = &#10;        \left( \begin{array}{c}&#10;           \alpha_1 \mathbf{u} \\&#10;           \alpha_1 \rho_1 \mathbf{u} \\&#10;           \alpha_2 \rho_2 \mathbf{u} \\&#10;           \rho \mathbf{u} \otimes \mathbf{u} + p \mathbf{I}\\&#10;           (\rho E + p) \mathbf{u}&#10;        \end{array} \right)&#10;    \mathbf{S} = &#10;        \left( \begin{array}{c}&#10;           \alpha_1 \nabla \cdot \mathbf{u} \\&#10;           0 \\&#10;           0 \\&#10;           0 \\&#10;           0&#10;        \end{array} \right)&#10;$$" src="svgs/e17a3de7478e3ea4b1124d2aaf70c7cb.png" align="middle" width="417.48629999999997pt" height="98.63106pt"/></p>

where <img alt="$\rho$" src="svgs/6dec54c48a0438a5fcde6053bdb9d712.png" align="middle" width="8.498985000000003pt" height="14.155350000000013pt"/> is the mixture density, <img alt="$\mathbf{u}$" src="svgs/129c5b884ff47d80be4d6261a476e9f1.png" align="middle" width="10.502250000000002pt" height="14.61206999999998pt"/> the mixture velocity, <img alt="$E$" src="svgs/84df98c65d88c6adf15d4645ffa25e47.png" align="middle" width="13.082190000000004pt" height="22.46574pt"/> the total energy, <img alt="$p$" src="svgs/2ec6e630f199f589a2402fdf3e0289d5.png" align="middle" width="8.270625000000004pt" height="14.155350000000013pt"/> the pressure, and <img alt="$rho_i$" src="svgs/b921dbff3fd97c42704607ee82ee7cc8.png" align="middle" width="29.96301pt" height="22.831379999999992pt"/> and <img alt="$\alpha_i$" src="svgs/67e7dd600dde6ca2d15b4df76a96110b.png" align="middle" width="15.166635000000003pt" height="14.155350000000013pt"/> are the density and volume fraction of each phase. 




## Citation
If you use this code for your work or research, please cite this repository:

```
@software{heylmun_blastfoam:_2019,
	title = {{blastFoam}: An {OpenFOAM} Solver for Compressible Multi-Fluid Flow with Application to High-Explosive Detonation},
	url = {https://github.com/synthetik-technologies/blastfoam},
	publisher = {Synthetik Applied Technologies, {LLC}.},
	author = {Heylmun, Jeffrey and Vonk, Peter and Brewer, Timothy},
	date = {2019-10-22}
}
```
