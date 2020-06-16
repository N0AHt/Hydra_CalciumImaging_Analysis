# Hydra_CalciumImaging_Analysis
A Pipeline for the automated analysis of calcium imaging data from Hydra Vulgaris.

This package allows the automated extraction of calcium imaging data - such as relative fluorescence and deconvolved spike times - from our 2-colour line of Hydra Vulgaris.

This allows large datasets of activity from hundreds of neurons to be generated, and the package provides many tools to aid in the visualization of this data and the many correlations which may occur within these datasets.

Our paper on the subject can be found ...


## Requirements

[Anaconda](https://www.anaconda.com/) - Tested with Ver. 4.8.3

Used for package management and installation of the required dependencies for this project. Other environment managers could also be used.
---
  **NOTE** If using an alternate Anaconda version, different commands may be needed to generate an environment from the provided .txt files.
---

[FFMPeg](https://ffmpeg.org/download.html)

Provides support for the image processing tools in this package.

[Icy](http://icy.bioimageanalysis.org/)

Provides the point tracking algorithm used to track neurons throughout a recording.

---
  **NOTE** Additional plugins for ICY may be required - please see the full [installation guide](Installation/README.md) for details.
---


## Installation Guide

Anaconda can (and most likely should) be used to create an environment and install the required dependencies to use this code.

* Download this repository as a zip and extract the files
* Open the Anaconda Prompt and navigate (using the cd command) into the installation folder of the repository. For example:
  * `cd Desktop`
  * `cd Hydra_CalciumImaging_Analysis\Installation`
* Create the Anaconda Environment using:

```bash
conda create --name Hydra_Analysis --file hydra_env_win10.txt
```
Using the correct .txt file for your operating system.

For more information on installation, and for installing additional packages, see [here](Installation/README.md)

## Using the Pipeline

**Getting Started**

**Usage and Development**

## Acknowledgements

### Dependencies

Can be downloaded and installed using the provided .txt files for Windows10, MacOS, and Ubuntu
