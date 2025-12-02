# GFlowNet for Causal Synthetic Data in Rare Diseases

This project builds a small GFlowNet setup that can create synthetic health records for rare disease research. The aim is to give a way to make new data while keeping key causal links from the real dataset. This can help when the true data is too small, too private, or too hard to share.

The notebook shows how to train a simple GFlowNet to sample from a user-defined causal graph, then generate new records that follow the same cause-and-effect rules.

## What this project includes

1. A toy causal graph for a rare disease setting.
2. A small dataset built from that graph.
3. A simple GFlowNet model in PyTorch.
4. Training code with step-by-step comments.
5. A script to measure how close the synthetic samples are to the real data.
6. Notes on limits and safe use.

The goal is to give a clean starting point that others can read and test. The code is short and does not need much setup.

## Why this matters

Rare diseases often have very small patient groups. That makes it hard to train ML models or share data across sites. Classical synthetic data tools may break cause-and-effect links. This small project shows how a GFlowNet can keep those links by sampling from a graph that encodes them.

## Setup

You can run the notebook on Google Colab.

Requirements:

* Python 3.9 or newer
* PyTorch
* NetworkX
* NumPy
* Matplotlib

If you are in Colab, the notebook will install anything that is missing.

## How to run

1. Open the notebook.
2. Run the environment setup cell.
3. Look at the causal graph section.
4. Run the data build step.
5. Train the GFlowNet.
6. Use the sampling cell to make synthetic records.
7. Check the plots that compare true and synthetic data.

## Notes on safe use

* The demo data is fake.
* Real health data needs care, strong checks, and review from domain experts.
* Synthetic samples can still leak info if the setup is poor.
* Always test if the model copies any real record too closely.

## License

MIT License.
