# PODE-HRM-MLP-AutoIgnition-Surrogate

This repository provides the reproducibility package for the manuscript:

**Fast Auto-Ignition Prediction of PODE Fuels Using HRM-Trained Neural Networks**

The repository contains dataset files, configuration details, model-training placeholders, inference benchmarking utilities, and supporting documentation for HRM-trained MLP surrogate modelling of PODE3/PODE4 auto-ignition.

## Repository Purpose

The purpose of this repository is to support reproducibility of the proposed data-driven surrogate framework for predicting ignition-relevant thermochemical outputs of PODE3/PODE4–air mixtures under compression-ignition-relevant conditions.

The surrogate model uses a partitioned multilayer perceptron (MLP) framework trained on homogeneous reactor model (HRM)-style ignition trajectories. The model input variables include:

- Degree of polymerization: `PODEn`
- Progress variable: `Yc`
- Mixture fraction: `Z`
- Normalized initial absolute enthalpy: `H_norm`

The predicted outputs include:

- Temperature and pressure
- Product species mass fractions
- Educt species mass fractions
- Heat release rate

## Important Note

The current dataset is a synthetic HRM-style reproducibility scaffold generated according to the variables and qualitative ignition trends described in the manuscript. It is intended to organize the reproducibility workflow and demonstrate the expected data format.

If actual Cantera/HRM simulation outputs are available, the CSV files in the `dataset/` directory should be replaced with the real HRM-generated dataset before final publication.

## Repository Structure

```text
PODE-HRM-MLP-AutoIgnition-Surrogate/
│
├── dataset/
│   ├── train.csv
│   ├── validation.csv
│   ├── test.csv
│   └── dataset_summary.csv
│
├── config/
│   └── dataset_config.json
│
├── scripts/
│   ├── generate_dataset.py
│   ├── train_mlp.py
│   ├── test_metrics.py
│   └── inference_benchmark.py
│
├── models/
│   └── [trained model weights to be added]
│
├── requirements.txt
├── checksums_sha256.json
└── README.md
