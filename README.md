# Learning function from structure in neuromorphic networks


## "What's in this repository?"

This repository contains code for the manuscript "[Learning function from structure in neuromorphic networks](https://www.biorxiv.org/content/10.1101/2020.11.10.350876v1)" by Laura Suarez, Blake Richards, Guillaume Lajoie & Bratislav Misic.

We investigated the link between macroscale connectivity and the computational properties that emerge from network dynamics in the human connectome.

We've tried to document the various aspects of this repository with this README file, so feel free to check things out!

This repository can be referenced using [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4776829.svg)](https://doi.org/10.5281/zenodo.4776829)

## "How to run the things from scratch?"

First, you'll need to make sure you have installed the appropriate software packages, and have downloaded the appropriate data files.

1. Git clone the [suarez_neuromorphicnetworks](https://github.com/netneurolab/suarez_neuromorphicnetworks.git) repository.
2. Download the "data" and "raw_results" folder from [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4776453.svg)](https://doi.org/10.5281/zenodo.4776453) and place them into the repository's root directory.
3. In the command line, type:

```bash
cd suarez_neuromorphicnetworks
conda env create -f environment.yml
conda activate rc
```

4. Git clone [reservoir](https://github.com/estefanysuarez/reservoir.git) repository.
5. And install it in the newly created environment:
```bash
cd reservoir
pip install .
```

4. Then, follow these steps sequentially (i.e., first "Run simulations", then "Compile results" and then "Analyses and Figures").

### Step 1. Run simulations
```bash
python scripts/01_rc_workflow/1_run_rc_workflow.py

python scripts/01_rc_workflow/2_get_network_properties.py
```

### Step 2. Compile results
```bash
python scripts/02_fetch_results/fetch_task_results.py

python scripts/02_fetch_results/fetch_net_props_results.py
```
### Step 3. Analyses and figures
```bash
python scripts/03_analysis/figX.py
```
(replace X by the number of the figure)


## "How to run only the analyses?"
1. Git clone the [suarez_neuromorphicnetworks](https://github.com/netneurolab/suarez_neuromorphicnetworks.git) repository.
2. Download the "data" and "proc_results" folders from [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4776453.svg)](https://doi.org/10.5281/zenodo.4776453) and place them into the repository's root directory.

To run the analysis presented in Figure "X" of the manuscript, you just need to run:

```bash
python scripts/03_analysis/figX.py
```


## From the paper - where to get stuff

### Data availability

The source dataset from University of Lausanne is available at https://doi.org/10.5281/zenodo.2872624. To facilitate the reproducibility of this work, the data ready to run the code is publicly available on Zenodo (https://doi.org/10.5281/zenodo.4776453).

### Code availability

All code used for data processing, simulation, analysis, and figure generation is publicly available on GitHub and Zenodo (https://github.com/netneurolab/suarez_neuromorphicnetworks; https://doi.org/10.5281/zenodo.4776829)172, and is built on top of the following open-source Python packages: reservoir (https://github.com/estefanysuarez/reservoir; https://doi.org/10.5281/zenodo.4913398), Netneurotools (https://github.com/netneurolab/netneurotools), Numpy173,174,175, Scipy176, Pandas177, Scikit-learn178, bctpy (https://github.com/aestrivex/bctpy)89, NetworkX 179, Matplotlib180 and Seaborn181.

