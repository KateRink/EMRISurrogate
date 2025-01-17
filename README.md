# EMRISurrogate

Copyright (c) 2020 Black Hole Perturbation Toolkit Team

The EMRISurrogate package provides access to a surrogate gravitational
waveform model. Currently, this package supports one model, EMRISur1dq1e4,
for non-spinning black hole binary systems with mass-ratios varying from 3 to
10000. This surrogate model is trained on waveform data generated by
point-particle black hole perturbation theory (ppBHPT), with the total mass
rescaling parameter tuned to NR simulations according to equation 4 of
paper 1 (see citations below).

This total mass rescaling is applied in the function slog_surrogate, and
so to generate point-particle perturbation theory waveforms without any
tuning to NR set alpha = 1 in the relevant function. Note that alpha
approaches unity in the extreme mass ratio limit.

Available modes are [(2,2), (2,1), (3,3), (3,2), (3,1), (4,4), (4,3), 
(4,2), (5,5), (5,4), (5,3)]. The m<0 modes are deduced from the m>0 modes.

Model details can be found in paper 1 (see citations below). 

## Getting the package

The latest development version will always be available from the project git
repository:

```bash
git clone https://github.com/BlackHolePerturbationToolkit/EMRISurrogate.git
```

# Requirements

This package requires Python 3 and the sklearn package. Parts of the accompanying
Jupyter notebook will require gwsurrogate, which can be installed with 

```bash
pip install gwsurrogate
```

Note that you do not need gwsurrogate to evalulate the EMRI surrogate model or 
run most parts of the notebook.

# Installation

1. Clone the repository
2. Download the datafile (hosted on [Zenodo](https://zenodo.org/record/3612600#.YYPdG3VKg5k))

```bash
wget https://zenodo.org/record/3612600/files/EMRISur1dq1e4.h5
```

3. Create a static link from in the main directory to the EMRISur1dq1e4.h5 file.
Or simply move the EMRISur1dq1e4.h5 file into the main directory.

# Usage

Please see the accompanying Jupyter notebook

```bash
jupyter notebook EMRISur1dq1e4.ipynb
```

# Examples

Examples are included in the Jupyter notebook.

# Known problems

Known bugs are recorded in the project bug tracker:

https://github.com/BlackHolePerturbationToolkit/EMRISurrogate/issues


# License

This code is distributed under the MIT License. Details can
be found in the LICENSE file.


# Authors

Scott Field  
Tousif Islam  
Gaurav Khanna  
Nur Rifat  
Vijay Varma

# Citation guideline

If you make use of any module from the Toolkit in your research please acknowledge using:

> This work makes use of the Black Hole Perturbation Toolkit.

If you make use of the EMRI surrogate model, EMRISur1dq1e4, please cite Paper 1:

```
@article{rifat2019surrogate,
  title={A Surrogate Model for Gravitational Wave Signals from Comparable-to Large-Mass-Ratio Black Hole Binaries},
  author={Rifat, Nur EM and Field, Scott E and Khanna, Gaurav and Varma, Vijay},
  journal={arXiv preprint arXiv:1910.10473},
  year={2019}
}
```
