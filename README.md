# GSoC 2026 – Brain-to-Brain Decoder Tasks and Proposal

This repository contains my implementation for the **Brain-to-Brain Decoder (Validating Neural Synchrony Patterns in Human Conversation)** test and proposal for **Google Summer of Code 2026** under **ML4SCI**.

## Problem Statement

You can view the official problem statement [here](https://docs.google.com/document/d/1eW2O4zgUFMa_OM0MspsssCqMIbONZg1pPRmfsMm6H2Y/edit?tab=t.0).

## General Approach

| Task | Description |
| --- | --- |
| **Part 1** | **Preprocessing**: Segmented EDF data (cropped positive & negative affect), removed VREF channel, and performed artifact removal using ICA. Compared power spectra before and after ICA. |
| **Part 2** | **CEBRA Embedding**: Concatenated preprocessed 64-channel datasets, Z-normalized across time, and applied CEBRA with 3-dimensional output embeddings. Evaluated using KNN decoding accuracy and goodness-of-fit score, along with a shuffled-data control. |
| **Part 3** | **Interpreting the Embedding**: Analyzed the embedding geometry (transitions, dense regions) and the shuffled-data control analysis results. |
| **Part 4** | **Reflection**: Identified specific limitations of the analysis given the data and choices, and discussed potential improvements if given more time and data. |

## Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/GSOC-NeuroDyads
cd GSOC-NeuroDyads
```

### 2. Create and activate the Conda environment

Make sure you have Conda installed. Then run:

```bash
conda env create -f environment.yml
conda activate neurodyads_task
```

### 3. Download Datasets

Below are the datasets required for the tasks:

- **Raw EEG Files (EDF)** – Box Link: [Alabama Box](https://alabama.box.com/s/gjdws83el45i1f99wt5qvmcmaspazpfe)

Please download and place these datasets in the corresponding `data/` folders.