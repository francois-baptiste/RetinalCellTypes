# Retinal Cell Types

This repository provides code accompanying the paper "The emergence of multiple retinal cell types through
efficient coding of natural movies," presented at NeurIPS 2018: https://www.biorxiv.org/content/early/2018/10/31/458737

### Optimization of Linear Cell Types (semi-analytical solution using a grid search)

C4_RFs.ipynb: Optimal spatio-temporal RFs of one and two types for a given firing rate budget (fig. 3abc)

C3_RATIO_SLIDER_VAR.ipynb: Reconstruction error as a function of the fraction of 'midget' cells at fixed Root-Mean-Squared (RMS) firing rate budget (fig 3d).

C4_RATIO_SLIDER_SPIKES.ipynb: RMS firing rate budget as a function of the fraction of 'midget' cells at fixed reconstruction error (fig 3e).

C5_ECCENTRICITY.ipynb: Optimal fraction of 'midget' cells and total density of cells as a function of firing rate budget. Comparison with these same quantities measured at all retinal eccentricties (fig. 3f). 1 dimension in space, 1 dimension in time.

C6_ECCENTRICITY_2d.ipynb: Version of the C5_ECCENTRICITY.ipynb with 2 dimensions in space and 1 dimension in time (Section 4, data not shown).

C6_WF_CONV_2TYPES.ipynb: Numerical simulation based on gradient descent showing that even when we allow the two cell types to share spatio-temporal modes (i.e. they both encode the same mode in their RF), the optimization chooses not to do so (appendix E).

C1_SPEEDY_WF.pynb: Reconstruction error with respect to RMS firing rate budget for one or two types (fig. 6c)


### Optimization Of Non-Linear Cell Types with a Neural Network Simulation

NeuralNetSimulation.py contains the code needed to train the nonlinear neural network models referred to in the paper.   It runs on a GPU using Keras with Tensorflow backend.  The code runs properly using Python 3.5.2, Tensorflow 1.1.0, Cuda 8.0, and Keras 2.1.3 (other versions may work as well but there is no guarantee). It performs a grid search over possible cell type allocations (number of cells for each type), noise values, and l1 regularization values.  Stores the results in a numpy array which can be processed using Jupyter notebook AnalyzeNeuralNetSimulation.ipynb.

AnalyzeNeuralNetSimulation.ipynb contains code used to plot all neural network-related results in the paper.  Comments in the code describe the role of each part and refer to particular figures in the paper.

### Other

C6_POWER_ILLUSTRATION.ipynb: Illustration of natural movie statistics (fig. 1b)

