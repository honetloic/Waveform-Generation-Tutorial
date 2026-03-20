# Waveform-Generation-Tutorial

## Goal

The goal of this tutorial is to familiarize yourself with modern tools for generating and comparing waveforms.

We will be generating waveforms from three different classes of models: effective-one-body (EOB), numerical relativity (NR) and self-force (SF) models. We will then extract from those waveform important quantities such as fluxes, mode amplitudes, QNM frequencies etc. Finally, we will compute mismatch between different model's waveforms.

## Installation

We will install the different packages in a virtual environment using conda. Before installing the different waveform packages, make sure you have conda installed (see the installation procedure [here](https://www.anaconda.com/docs/getting-started/miniconda/install/overview)).
If you have experiences with another specific package manager, feel free to use it instead.

Open a terminal, and create a virtual environment for this tutorial:
```bash
conda create --name GWTutorial
```
Then activate the environment with 
```bash
conda activate GWTutorial
```
Next, we will need to install the pyseobnr python package. For that we will first install lalsuite, as it will automatically install the necessary dependencies for pyseobnr:

```bash
conda install -c conda-forge lalsuite
```
Then install pyseobnr from source

```bash
git clone https://git.ligo.org/waveforms/software/pyseobnr.git
cd pyseobnr
pip install -U pip wheel setuptools numpy
pip install .
cd ..
```
(see [installation guideline](https://waveforms.docs.ligo.org/software/pyseobnr/source/installation.html) if you encounter issues). Now, we install the sxs (NR simulations catalog) python package and its dependencies
```bash
conda install -c conda-forge sxs 
```
(or follow this [installation guide](https://sxs.readthedocs.io/en/main/)).

We will also install FEW (FastEMRIWaveforms) for generating self-force waveform models. This is easily done with pip
```bash
pip install fastemriwaveforms
```
(see [installation guidelines](https://github.com/BlackHolePerturbationToolkit/FastEMRIWaveforms)).

Finally, make sure you have some way of running interactive notebooks. You may want to install [jupyter](https://jupyter.org/install) as well as [VScode](https://code.visualstudio.com) as a code editor.

With all of this, you are now ready to tackle the third GW exercise session.