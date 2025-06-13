# Fluid Dynamics Measurements using Deep Learning-Based Optical Flow Models

This repository contains datasets and pre-trained models used in the study **"Fluid Dynamics Measurements using Deep Learning-Based Optical Flow Models"**, which integrates deep learning and classical optical flow methods (DOF, SPyNet, RAFT) into Particle Image Velocimetry (PIV) workflows.

## 📁 Repository Structure

├── dataset/

│ ├── synthetic_translational/ # Synthetic plug flow (10 samples)

│ ├── synthetic_rotational/ # Synthetic vortex flow (10 samples)

│ ├── jet_plug_flow_re_1100/ # Experimental jet flow, Re=1100 (200 frames)

│ ├── jet_plug_flow_re_2200/ # Experimental jet flow, Re=2200 (200 frames)

│ ├── PIV_challanges/Ball/ # Benchmark PIV dataset (e.g., Case B)

│ └── RAFT_trained_data/uniform/ # Synthetic uniform dataset for RAFT training (3000 samples)

 └── RAFT_trained_data/DNS_turbulance/ # Turbulance dataset for RAFT training (2000 samples)
 

├── models/
│ ├── DOF/ # Pre-processing code or configs for Dense Optical Flow
│ ├── SPYNET/ # Pre-trained weights or scripts
│ ├── RAFT/ # Vanilla RAFT model
│ └── Fine_tune_RAFT/ # Domain-adapted RAFT model fine-tuned on synthetic flow

## 📊 Datasets

| Dataset Type       | Description                           | Frame Count |
|------------------- |---------------------------------------|-------------|
| Synthetic Flow     | Plug (translational) and vortex flow  | 10 each     |
| Jet Flow (PIV)     | Real experimental data (Re=1100/2200) | 200 each    |
| PIV Challenge      | Benchmark case (e.g., "Ball")         | Varies      |
| RAFT Training Data | Synthetic uniform translation         | ~3000       |
| RAFT Training Data | DNS turbulance translation            | ~2000       |
> 🧪 All datasets are either synthetically generated using MATLAB or obtained from high-resolution jet flow PIV experiments.

## 🤖 Optical Flow Models

The repository supports three main models:
- **DOF (Dense Optical Flow)** – Based on Farnebäck’s algorithm.
- **SPyNet** – A lightweight, pyramidal deep neural network for optical flow.
- **RAFT** – A high-accuracy deep learning method; includes a fine-tuned version for domain-specific velocity fields.

## 📈 Applications

These datasets and models can be used to:
- Benchmark optical flow algorithms in fluid dynamics
- Compare ML-based vs classical PIV measurements
- Train or evaluate flow estimation networks for laminar/turbulent regimes

## 🧷 License

This project is made available for academic and non-commercial use only.
