# Hydra_CalciumImaging_Analysis
A Pipeline for the automated analysis of calcium imaging data from Hydra Vulgaris.

This package allows the automated extraction of calcium imaging data - such as relative fluorescence and deconvolved spike times - from our 2-colour line of Hydra Vulgaris.

This allows large datasets of activity from hundreds of neurons to be generated, and the package provides many tools to aid in the visualization of this data and the many correlations which may occur within these datasets.

Our paper on the subject can be found ...


## Requirements

Anaconda - Tested with Ver. 4.8.3

FFMPeg

ICY

caiman

-note: if installing new packages to add to the code base, use the guide from caiman to ensure only conda-forge channel is used (recommended installations)

**Dependencies**

Can be downloaded and installed using the provided .yml files for Windows10, MacOS, and Ubuntu

## Installation Guide

Anaconda can (and most likely should) be used to create an environment and install the required dependencies to use this code.

* Download this repository as a zip and extract the files
* Open the Anaconda Prompt and navigate (using the cd command) into the installation folder of the repository. For example:
  * `< cd Desktop>`
  * `<cd Hydra_CalciumImaging_Analysis\Installation`>
* Create the Anaconda Environment using:

```bash
conda env create --file hydra_env_win10.txt
```

Using the correct .txt file for your operating system.

## Usage

**Getting Started**

**Usage and Development**
