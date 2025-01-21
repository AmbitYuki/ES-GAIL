# Distributed Adversarial Learning for Intelligent Power System Control

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📑 Introduction

This repository implements ES-GAIL (Energy System Generative Adversarial Imitation Learning), a distributed machine learning framework presented in our paper "Distributed Adversarial Learning for Parallel Computational Strategies in Intelligent Power System Control Optimization". 

ES-GAIL enables development of sophisticated control strategies for power generation systems without requiring explicit system modeling, leveraging the power of adversarial imitation learning.

## 🌟 Key Features

- **Hybrid Neural Architecture**: Combines convolutional and recurrent layers for comprehensive system modeling
- **Distributed Learning**: Scales efficiently across multiple computational nodes
- **Robust Control**: Demonstrates resilience against sensor failures and unseen scenarios
- **Data-Driven Approach**: Learns directly from system demonstrations without explicit modeling

## 🏗️ System Architecture

```
ES-GAIL
├── Convolutional Layers → Spatial relationship modeling
├── LSTM Layers → Temporal dynamics processing
├── Reward Modeling → Inverse reinforcement learning
└── Phased Training → Curriculum-based learning
```

## 📊 Performance Highlights

- Successfully controls combined cycle power plants following load demands
- Outperforms traditional control methods and other ML baselines
- Demonstrates robust generalization to unseen load profiles
- Maintains stability under simulated sensor failures

## 🗂️ Repository Structure

```
.
├── data/                   # Training and evaluation datasets
├── networks/              # Neural network architectures
│   ├── generator.py      # Hybrid conv-recurrent generator
│   ├── discriminator.py  # Discriminator network
│   └── reward_net.py     # IRL reward network
├── processing/           # Data processing utilities
├── main.py              # Training and evaluation script
└── run.sh               # Experiment runner
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- PyTorch 2.0+
- CUDA-capable GPU (recommended)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/username/ES-GAIL.git
cd ES-GAIL
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Prepare your data:
```bash
# Place your data files in the data/ directory
cp your_data.csv data/
```

4. Configure and run:
```bash
# Modify configuration as needed
vim run.sh

# Execute
./run.sh
```

## 📈 Results

Our experiments demonstrate that ES-GAIL achieves:
- Superior control performance compared to baseline methods
- Robust generalization to unseen operational scenarios
- Efficient computational scaling with system size
- Stable learning across different training configurations

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

