# MENP
Multipole Expansion for NanoPhotonics (MENP)  

## General
MENP is an open-source MATLAB-based package for multipole expansion based on induced displacement current in nanostructures. It imports electric field distribution obtained by full-field simulation techniques (e.g., FDTD, FEM, etc.) and computes electric and magnetic multipoles (ED, MD, EQ, MQ) based on exact expression of multipole expansion. It is also capable of multipole expansion under long-wavelength approximation to find a contribution of toroidal dipole moments (TD).

Target users are researchers in the field of nanophotonics. In particular, recently emerged sub-wavelength Mie resonators exhibit rich spectral features due to multipole resonances. The resultant multipolar interference is opening up new opportunities to realize novel functionarity such as unidirectinal scattering (so-called Kerker condition), non-radiating optical Anapole state, and so on. For structural design and interpretation of physics in such systems, full-field simulation accoumpanied by multipole expansion is essential.

This package is basically designed for the use with Lumerical FDTD solutions, but any software can be used by exporting four-dimensional (x,y,z,f) electric field and refractive index data as a MATLAB .mat file.

## References
[1] Alaee, R.; Rockstuhl, C.; Fernandez-Corbaton, I. An Electromagnetic Multipole Expansion beyond the Long-Wavelength Approximation. [Opt. Commun. 2018, 407, 17–21.](https://www.sciencedirect.com/science/article/pii/S003040181730754X)  
[2] Baryshnikova, K. V.; Smirnova, D. A.; Luk’yanchuk, B. S.; Kivshar, Y. S. Optical Anapoles: Concepts and Applications. [Adv. Opt. Mater. 2019, 7, 1801350.](https://onlinelibrary.wiley.com/doi/full/10.1002/adom.201801350)  
[3] Hasebe, H.; Sugimoto, H.; Hinamoto, T.; Fujii, M. Coupled Toroidal Dipole Modes in Silicon Nanodisk Metasurface: Polarization Independent Narrow Band Absorption and Directional Emission. [Adv. Opt. Mater. 2020, 2001148.](https://onlinelibrary.wiley.com/doi/full/10.1002/adom.202001148)

## License
MIT

## Author
Tatsuki Hinamoto@Kobe University, Japan

## How to use
See ./demo_sphere (for exact multipole expansion) and ./demo_disk (for approximate multipole expansion including toroidal moment).  

For the computation, electric field and refractive index data computed around a target nanostructure is required. On Lumerical FDTD Solutions, this export process can be done by running "./lumerical_script/EField2MAT.lsf". As an example, Lumerical project files (.fsp) are also included in the demo directories.