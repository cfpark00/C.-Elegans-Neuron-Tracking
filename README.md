# C.-Elegans-Neuron-Tracking
Various algorithms to track neurons in a deforming brain

## Hermaphrodite Detection

### Approximate Truth generation: mask-train-prepare.ipynb
This notebook generates an approximate truth to train a Neural Network

### Training U-Net: Seg-UNet.ipynb
This notebook trains a U-Net architecture to mask out the Hermaphrodite.

Implementation modified from: https://github.com/milesial/Pytorch-UNet

Original paper by Olaf Ronneberger, Philipp Fischer, Thomas Brox: https://arxiv.org/abs/1505.04597

### Applying U-Net: Apply-Mask.ipynb
This notebook applies the U-Net to images to mask out the Hermaphrodite

## Peak detection

### Analytic peak detection: Get-Peaks.ipynb
This notebook explains how to get peaks from raw images. This algorithm is very primitive and unstable.

## Worm Straightening

### Standard Posture generation: ground.ipynb
This notebook generates a standard posture to straighten the worms.

### Worm Straightening: straighten.ipynb
This notebook explains how to put all the peaks in a certain posture, described by a potential well.

## Segmentation
This part partially implements (without centerline detection and error correction):

Jeffrey P. Nguyen, Ashley N. Linder, George S. Plummer, Joshua W. Shaevitz, and Andrew M. Leifer: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5436637/

### Applying a Thin Plate Spline: TPS.ipynb
This part is a tiny modification of: https://github.com/bing-jian/gmmreg-python due to some memory leak issues.
This notebook explains the Thin Plate Spline Point Set Registration method.

### Neuron Segmentation: track.ipynb
This notebook explains the paper's method of constructing neuron registration vectors and clustering them.

Contact: corefranciscopark@g.harvard.edu / cfpark00@gmail.com

