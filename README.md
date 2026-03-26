# Triplet Loss Tutorial: How Triplet Selection Changes Embedding Quality

## Overview
This repository contains the code and tutorial materials for a machine learning tutorial on triplet loss and embedding learning. The project focuses on one question:

**How does triplet selection affect embedding quality?**

The experiment compares two training strategies:
- random triplet selection
- semi-hard triplet selection

The goal is to show how more informative triplets can improve the structure of the learned embedding space.


## Task summary
A small convolutional encoder is trained on a four-class subset of Fashion-MNIST. Both models use the same:
- dataset split
- encoder architecture
- embedding size
- optimizer
- triplet-loss margin
- number of epochs

The only difference is the triplet-selection strategy used during training.

The learned embeddings are evaluated using:
- k-nearest-neighbor accuracy in embedding space
- mean intra-class distance
- mean inter-class distance
- PCA visualization of embeddings

## How to run
1. Create and activate a Python environment.
2. Install the required packages:
   ```bash
   pip install -r requirements.txt                          Open the notebook:

Run all cells from top to bottom.                       

 outputs

Running the notebook should reproduce:

training loss curves
PCA embedding plots
distance distribution plots
summary evaluation table
Main finding

Both mining strategies learn useful embeddings, but semi-hard triplet selection produces slightly better embedding quality. It gives:

slightly higher k-nearest-neighbor accuracy
lower intra-class distance
higher inter-class distance
tighter and cleaner clusters in PCA plots

This suggests that triplet selection affects the geometric quality of the learned representation.

Accessibility

This project was prepared with accessibility in mind. The tutorial uses:

clear section headings
plain-language explanations
descriptive figure captions
readable labels in plots
simple table formatting

Visual conclusions are also explained in text so that interpretation does not depend only on images.

Reproducibility

The notebook uses a fixed random seed and a controlled experimental setup so that the effect of triplet selection can be isolated as clearly as possible.

License
MIT.


