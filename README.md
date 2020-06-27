# Hydra_CalciumImaging_Analysis
A Pipeline for the automated analysis of calcium imaging data from Hydra Vulgaris.

This package allows the automated extraction of calcium imaging data - such as relative fluorescence and deconvolved spike times - from our 2-colour line of Hydra Vulgaris.

This allows large datasets of activity from hundreds of neurons to be generated, and the package provides many tools to aid in the visualization of this data and the many correlations which may occur within these datasets.

Our paper on the subject can be found ...


## Requirements

Please install the following software prior to using this package:

[Anaconda](https://www.anaconda.com/) - Tested with Ver. 4.8.3

Used for package management and installation of the required dependencies for this project. Other environment managers could also be used.

  **_NOTE:_** If using an alternate Anaconda version, different commands may be needed to generate an environment from the provided .txt files.


[FFMPeg](https://ffmpeg.org/download.html)

Provides back-end support for the image-processing tools used in this package.

[Icy](http://icy.bioimageanalysis.org/)

Provides the point tracking algorithm used to track neurons throughout a recording.

  **_NOTE:_** Additional plugins for ICY may be required - please see the full [installation guide](Installation) for details.


## Installation Guide

Anaconda can (and most likely should) be used to create an environment and install the required dependencies to use this code.

* Download this repository as a zip and extract the files
* Open the Anaconda Prompt and navigate into the installation folder of the repository. For example:
  * `cd Desktop`
  * `cd Hydra_CalciumImaging_Analysis\Installation`
* Create the Anaconda Environment using:

```bash
conda create --name Hydra_Analysis --file hydra_env_win10.txt
```
Using the correct .txt file for your operating system.

For more information on installation, and for installing additional packages, see [here](Installation)

## Using the Pipeline

### Getting Started

The pipeline is designed to analyse videos generated from a 2-colour line of Hydra, expressing both a calcium-sensitive indicator and a calcium insensitive indicator in their neurons. Once a recording has been taken of both channels using a 2-colour microscope, the calcium insensitive recording should be imported into Icy and its spot tracker function used. The results of this can be exported as a .csv file for analysis with this program. Note, trimming videos in icy will result in more neurons being tracked. There is an inverse relationship between length of video and number of points tracked successfully. The video recordings should be converted into .avi files prior to starting analysis. Once this is complete the two .avi files (one for each colour channel) and the .csv from Icy can be used to analyse the neural activity.

To test your installation and see how the code is designed to work, an [example dataset](Example_Data) is provided. This can be used with the provided jupyter notebook (Single_Cell_Hydra_Analysis.ipynb).

Although this notebook is designed to contain ample internal instruction for its use, there are a few steps to take before attempting to run it:

1. Ensure you have downloaded FFMPeg and anaconda
2. Clone this repo (or download as a zip and unzip it)
3. Follow the installation guide to create the required environment for your operating system
4. Activate the environment with the command:
  ```bash
  conda activate Hydra_Analysis
  ```
5. Open Jupyter (note that jupyter requires a browser - i.e. google chrome - to run):
  ```bash
  jupyter notebook
  ```
6. Find the Single_Cell_Hydra_Analysis.ipynb file and open it

**_NOTE:_** Jupyter may also be opened using the Anaconda Navigator - making sure to change environments using the drop down tab in the application before opening Jupyter.

### Using the Notebook

Once the notebook is opened most of the user input will be choosing parameters and entering the paths to the files you want to analyse. Most information is contained within the notebook, but some key points are:

* Update the paths for the two .avi files and the .csv file from icy to where they are stored on your machine.

**_NOTE:_** Paths on a windows machine need an r character preceding them to be read correctly, i.e.: r"c:\\user\files"

* Update the path to FFMPeg in the import cell. Copy and paste the path to the bin folder in the FFMPeg folder wherever that is on your machine. I would recommend resetting the kernel in the notebook after updating this path then re-running the cells from the beginning.

* Much of the other user input will be setting parameters to optimise your results. There are cells at the end of the notebook to evaluate these parameters and aid you in tuning the notebook to your data. It is recommended to run the notebook once then go back and tune each parameter individually, then reset the kernel and run the notebook again.

## Acknowledgements
other paper...
caiman...
masters thing...

### Dependencies

The initial code base for this project utilises the [CaImAn](https://github.com/flatironinstitute/CaImAn) package for its spike deconvolution functionality.
