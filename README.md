# Data export from Nf = 2+1+1 rho resonance

This repository contains the center of mass energy levels determined from the scattering of two pions at *I* = 1. The ensembles are the 2+1+1 flavor twisted mass ensembles by the ETMC. If you are using this data please cite https://arxiv.org/abs/2006.13805.

## Data format

The data is presented in a directory hierarchy with the following levels:

- On the first level there are directories `single` and `shifted`. These refer to the thermal state removal. In `single` no thermal state removal has been performed. The energies might be a little too low as thermal states pull them down. In `shifted` the weight-shift-reweight procedure has been applied before the energies were extracted. There the energies as likely a bit higher (more realistic), but the statistical uncertainties are also higher.

- The directories on the next levels refer to the ETMC ensembles and have a lattice spacing letter (`A` is coarse, `B` in the middle and `D` is fine). The number refers to the bare light quark mass and is a proxy for the pion mass.

- The first name group (with underscores) of the file is the moving frame, *P*² as `D\d` in regular expression notation.

- The second group is the lattice irrep.

- The third group redundantly states the `P_x`, `P_y` and `P_z` components of the total momentum. We only use the reference momentum and resolve everything else with global lattice rotations.

- The last group just numbers the principal correlators or energy levels.

In each of the files there are two columns. The first one is the center of mass energy $aE$ in lattice units. The second column is the phase shift in radians. Each row is one of the bootstrap samples. As they are pseudo-bootstrap samples generated from the previous jackknife distribution with covariance, the central value is just the mean over all bootstrap samples.
