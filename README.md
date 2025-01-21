

```markdown
# Distributed Adversarial Learning for Intelligent Power System Control

This repository contains the code for the paper "Distributed Adversarial Learning for Parallel Computational Strategies in Intelligent Power System Control Optimization". The paper presents ES-GAIL, a distributed machine learning framework that utilizes adversarial imitation learning to develop control strategies for power generation systems without requiring explicit system modeling. 

## Overview

Complex energy infrastructure poses substantial computational challenges due to interconnected subsystem dynamics and nonlinear behaviors. ES-GAIL addresses this by employing a hybrid neural network architecture in the generative model to capture spatiotemporal dependencies, and incorporates a reward modeling technique based on inverse reinforcement learning to enable stable learning from demonstrations.

Key features:
- Convolutional layers to capture spatial relationships between subsystems 
- Recurrent LSTM layers to model temporal dynamics
- Inverse reinforcement learning to transform state sequences into reward signals
- Phased training curriculum for robust learning

## Results

Experiments demonstrate that ES-GAIL achieves state-of-the-art performance in controlling a combined cycle power plant to follow load demands, outperforming various baselines. The learned control policies generalize well to unseen load profiles and are robust to simulated sensor failures.

## Code Structure

- `data/`: Contains data for training and evaluation
- `networks/`: Defines the neural network architectures 
  - `generator.py`: Hybrid convolutional-recurrent generator model
  - `discriminator.py`: Discriminator model
  - `reward_net.py`: Inverse reinforcement learning reward network
- `processing/`: Data processing and loading utilities
- `main.py`: Main training and evaluation script
- `run.sh`: Example script to run experiments

## Getting Started

1. Install the required Python dependencies (PyTorch, NumPy, Pandas, etc.)
2. Prepare your data in the `data/` directory 
3. Modify `run.sh` to configure the desired experiments
4. Run the experiments: `./run.sh`

```
