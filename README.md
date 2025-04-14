# ABS-Q: A Deep Learning Framework for Quantum Error Mitigation

This repository provides implementations for **ABS-Q** (Analysis-by-Synthesis for Quantum outputs), a convolutional deep learning framework designed to recover correct output distributions from noisy quantum circuits. It also includes comparison baselines with two Hamming-spectrum-based methods: **HAMMER** and **QBEEP**.

---

## 📁 Contents

- `ABS3.ipynb`: Main Jupyter notebook for the ABS-Q model, including training, evaluation, and visualization.
- `Hammer_reconstruction.ipynb`: Code for reweighting noisy distributions using the HAMMER protocol.
- `QBEEP_reconstruction.ipynb`: Implementation of the QBEEP method using Poisson-based binning and Bayesian state graph modeling.
---

## 🧠 Project Summary

Quantum devices are inherently noisy, especially in the Noisy Intermediate-Scale Quantum (NISQ) era. ABS-Q addresses the challenge of **recovering the correct output bitstring** from corrupted distributions produced by quantum machines. Our method uses convolutional layers that are Hamming-aware, allowing the model to exploit local and non-local error clustering across the Hamming spectrum.

The project includes:
- A custom convolutional architecture where node connections are determined by Hamming distance
- Evaluation using datasets generated from running 9-bit Bernstein–Vazirani circuits on IBM quantum devices
- Comparisons with HAMMER and QBEEP error mitigation strategies
- Metrics including precision, fidelity, rank improvement, and more

---

## 📊 Results Overview

ABS-Q outperforms HAMMER and QBEEP in:
- Precision and fidelity recovery
- Ranking improvement of correct bitstring
- Generalization across datasets with different Hamming weights
