# Global Modelling of Ganymede's Surface Composition
Supplementary material for King & Fletcher (2022):

*Global MCMC Modelling of Ganymede's Surface Composition: Near-IR Mapping from VLT/SPHERE*

Oliver King & Leigh Fletcher

[![DOI](https://zenodo.org/badge/475012230.svg)](https://zenodo.org/badge/latestdoi/475012230)

## Description
Files starting with `reflectance_` provide mapped spectral reflectance data for the VLT/SPHERE and Galileo/NIMS datasets used in this study.

Files starting with `fit_` provide mapped MCMC compositional fit results for the VLT/SPHERE and Galileo/NIMS datasets used in this study. The fit results contain the fitted best estimate abundances and 1-sigma upper and lower bound abundances calculated from the posterior abundance distribution for each endmember at each observed location.


## Data format
These files are saved as compressed (gzipped) [JSON](https://www.json.org) data files.

All major programming languages provide support for reading JSON files. The code snippet below shows an example of how to directly open and use these data files in Python:
```python
import json
import gzip

with gzip.open('fit_SPHERE.json.gz', 'r') as f:
    data = json.load(f)

print(data.keys()) # print structure of data file
print(data['description'])
```
