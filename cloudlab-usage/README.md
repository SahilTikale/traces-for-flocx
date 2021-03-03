# cloudlab-usage

This repository contains data and code involved in the analysis of ClodLab's 
control framework, facility usage, and its users. 

The structure of the repository is the following:

- `data/*.csv` files contain CloudLab usage data extracted from the live production databases powering the facility. 
  To preserve user identities, we excluded columns such as user names, used repositories and scripts, manifests, etc.
  and hashed the rest of sensitive information. For details of this anonymization process, refer to
  `sql2csv.ipynb` and `manifests2hardware.ipynb` notebooks. The latter processes all manifests 
  and extracts and saves information about the hardware used in each experiment. 
- `usage.ipynb` notebook contains code for analysis of CloudLab usage, from hardware types to reservations.
  This notebook loads all CSV files, displays important statistics, and produces many figures 
  characterizing system's utilization.

## Reproducing Results

Use the button shown below to run analysis notebooks from this repository using Binder. 

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/git/https%3A%2F%2Fgitlab.flux.utah.edu%2Femulab%2Fcloudlab-usage/3736456271eb98e1961b058e04f7e46822953cab)
