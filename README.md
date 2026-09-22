# Multi-Omics and Neuronal Dynamics Analysis in Alzheimer's Disease

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Biopython](https://img.shields.io/badge/Biopython-1.88-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

This repository contains the computational pipeline and empirical analyses developed for the **"From DNA to Data"** Capstone Project. The research integrates genomic sequence processing, differential gene expression profiling, biophysical neuronal simulations, and electrophysiological signal processing to investigate molecular mechanisms underlying Alzheimer's Disease (AD).

---

##  Project Overview

Alzheimer's Disease is characterized by complex interactions between gene dysregulation and neuronal dysfunction. This project bridges molecular genetics and neurophysiology through a four-stage computational approach:

1. **Genomic Sequence Processing (`Biopython`):** Automated fetch and analysis of human *BDNF* mRNA sequence.
2. **Differential Gene Expression (`Pandas`, `SciPy`):** Comparative expression profiling and independent $t$-tests for *BDNF*, *APOE*, and *APP* across Healthy vs. AD cohorts.
3. **Biophysical Neuronal Dynamics (LIF Simulation):** Modeling the physiological impact of *BDNF* depletion on action potential generation using Leaky Integrate-and-Fire models.
4. **Electrophysiological Signal Processing (FFT Analysis):** Spectral decomposition of synthetic EEG signals using Fast Fourier Transform.

---

## Key Findings & Results

### 1. Differential Gene Expression Analysis
Statistically significant expression shifts were observed across the target gene panel ($p < 0.001$):
* **BDNF:** Suppressed in AD cohort (Mean Healthy: $6.5 \rightarrow$ Mean Patient: $2.13$, $p = 7 \times 10^{-6}$) — indicates lost neuroprotective support.
* **APOE & APP:** Markedly elevated in AD cohort ($p < 10^{-5}$) — aligns with progressive amyloid pathology and lipid transport disruption.

### 2. Leaky Integrate-and-Fire (LIF) Simulation
* **Healthy Neurons ($\text{leak} = 0.05$):** Sustained membrane potential buildup achieving the $1.0\text{ V}$ threshold, generating regular action potential spikes.
* **BDNF-Depleted Neurons ($\text{leak} = 0.14$):** Elevated membrane leakiness prevents threshold attainment, resulting in complete failure of action potential firing.

### 3. EEG Frequency Spectrum
Fast Fourier Transform ($\text{rfft}$) resolved discrete spectral peaks at **$10\text{ Hz}$ (Alpha rhythm)** and **$20\text{ Hz}$ (Beta rhythm)** amidst Gaussian noise, validating signal recovery pipelines.

---

##  Visualizations

Generated figures illustrating key analytical stages:

| Gene Expression Heatmap | Neuronal Firing Dynamics | EEG Frequency Spectrum |
| :---: | :---: | :---: |
| `gene_heatmap.png` | `neuron_dynamics.png` | `eeg_spectrum.png` |
| Differential expression of BDNF, APOE, APP | Healthy vs. BDNF-deficient spike generation | Alpha (10 Hz) & Beta (20 Hz) FFT isolation |

---

##  Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Alzheimer-Bioinformatics-Analysis.git](https://github.com/YOUR_USERNAME/Alzheimer-Bioinformatics-Analysis.git)
   cd Alzheimer-Bioinformatics-Analysis
