# 🌌 Quantum Federated Learning Platform

A production-ready application combining **quantum computing** with **federated learning** to explore privacy-preserving machine learning with quantum advantage.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Qiskit](https://img.shields.io/badge/Qiskit-1.0+-purple.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 🚀 Features

- **Real Quantum Circuits**: IBM Qiskit integration with genuine quantum gates (RX, RY, RZ, CNOT)
- **Federated Learning**: Distributed training across multiple clients with parameter aggregation
- **Hybrid Architecture**: Quantum-classical neural networks with trainable parameters
- **Fallback Mode**: Classical simulation when Qiskit unavailable
- **Interactive GUI**: Full-featured Tkinter interface with real-time training visualization
- **Dataset Support**: Built-in quantum-optimized datasets (XOR, AND, OR) + CSV upload
- **Privacy-Preserving**: Federated approach keeps data local, shares only model parameters

## 🎯 Key Capabilities

✅ Variational quantum circuits with parameter-shift rule gradients  
✅ Quantum entanglement for feature correlation modeling  
✅ Angle encoding for classical-to-quantum data mapping  
✅ Federated averaging of quantum parameters  
✅ Real-time training metrics and convergence analysis  
✅ Comprehensive result visualization and export  

## 📦 Installation

### Quick Start (Simulation Mode)
```bash
# Clone the repository
git clone https://github.com/yourusername/quantum-federated-learning.git
cd quantum-federated-learning

# Install minimum dependencies
pip install numpy matplotlib pandas

# Run the application
python quantum_federated_learning.py
```

### Full Installation (Real Quantum Mode)
```bash
# Install all dependencies including Qiskit
pip install numpy matplotlib pandas qiskit qiskit-aer

# Run with real quantum circuits
python quantum_federated_learning.py
```

### Requirements
```
Python >= 3.8
numpy >= 1.21.0
matplotlib >= 3.5.0
pandas >= 1.3.0
qiskit >= 1.0.0 (optional - for real quantum)
qiskit-aer >= 0.13.0 (optional - for quantum simulation)
```

## 🖥️ Usage

### 1. Launch Application
```bash
python quantum_federated_learning.py
```

### 2. Configure Experiment
- **Quantum Status Tab**: Verify quantum backend (Qiskit or simulation mode)
- **Dataset Tab**: Select XOR/AND/OR datasets or upload custom CSV
- **Configuration Tab**: Set qubits (2-6), clients (2-5), rounds (3-20)

### 3. Run Training
- Click **"Start Quantum FL Training"** in Training Execution tab
- Monitor real-time metrics: accuracy, loss, quantum parameters
- View training logs with timestamped events

### 4. Analyze Results
- **Generate Report**: Comprehensive training summary with quantum metrics
- **Plot Results**: Visualize accuracy evolution and convergence
- **Export Data**: Save results as CSV for further analysis

## 🧪 Example: XOR Problem with Quantum Advantage
```python
# Built-in demonstration
1. Select "XOR Logic Gate" dataset (non-linearly separable)
2. Configure: 3 qubits, 3 clients, 8 rounds
3. Run training
4. Observe: Quantum circuits solve XOR better than classical linear models
```

**Why XOR?** The XOR problem is not linearly separable - perfect for demonstrating quantum superposition and entanglement advantages.

## 🏗️ Architecture
```
┌─────────────────────────────────────────────────────┐
│         Quantum Federated Learning Platform         │
├─────────────────────────────────────────────────────┤
│                                                     │
│  ┌──────────────┐      ┌──────────────┐            │
│  │   Client 1   │      │   Client 2   │  ...       │
│  │              │      │              │            │
│  │ ┌──────────┐ │      │ ┌──────────┐ │            │
│  │ │ Quantum  │ │      │ │ Quantum  │ │            │
│  │ │ Circuit  │ │      │ │ Circuit  │ │            │
│  │ │ (3 qubits)│ │      │ │ (3 qubits)│ │            │
│  │ └────┬─────┘ │      │ └────┬─────┘ │            │
│  │      │       │      │      │       │            │
│  │ ┌────▼─────┐ │      │ ┌────▼─────┐ │            │
│  │ │Classical │ │      │ │Classical │ │            │
│  │ │   NN     │ │      │ │   NN     │ │            │
│  │ └──────────┘ │      │ └──────────┘ │            │
│  └──────┬───────┘      └──────┬───────┘            │
│         │                     │                    │
│         └──────────┬──────────┘                    │
│                    │                               │
│            ┌───────▼────────┐                      │
│            │ Federated      │                      │
│            │ Averaging      │                      │
│            │ (Global Model) │                      │
│            └────────────────┘                      │
│                                                     │
└─────────────────────────────────────────────────────┘
```

### Quantum Circuit Design
```
    ┌──────┐     ┌──────────────────┐     ┌─────────┐
q_0:┤ RY(φ)├─────┤ RX(θ₀)RY(θ₁)RZ(θ₂)├──■──┤ Measure ├
    ├──────┤     ├──────────────────┤┌─┴─┐├─────────┤
q_1:┤ RY(ψ)├─────┤ RX(θ₃)RY(θ₄)RZ(θ₅)├┤ X ├┤ Measure ├
    └──────┘     └──────────────────┘└───┘└─────────┘
    
    Feature Encoding → Variational Layer → Entanglement → Measurement
```

## 📊 Datasets

### Built-in Datasets
- **XOR**: Non-linearly separable (quantum advantage)
- **AND**: Linearly separable (classical baseline)
- **OR**: Simple classification (baseline comparison)

### Custom Datasets
Upload CSV files with format:
```csv
feature1,feature2,...,target
0.5,0.8,...,1
0.2,0.3,...,0
```
- Last column = binary target (0/1)
- Features normalized automatically
- Multi-class converted to binary

## 🔬 Research Applications

- **Quantum Machine Learning**: Explore NISQ-era quantum algorithms
- **Privacy-Preserving ML**: Federated learning without data sharing
- **Quantum Advantage Studies**: Compare quantum vs classical on non-linear problems
- **Hybrid Systems**: Quantum-classical co-processing research
- **Educational Tool**: Learn quantum computing + federated learning

## 📈 Performance Metrics

The platform tracks:
- **Global Accuracy**: Aggregated model performance
- **Client Accuracy**: Individual client convergence
- **Quantum Parameters**: Circuit trainable parameters (3 × qubits)
- **Training Time**: Per-round and total execution time
- **Convergence Rate**: Accuracy improvement trajectory

## 🤝 Contributing

Contributions welcome! Areas for enhancement:
- Additional quantum encodings (amplitude, basis encoding)
- Noise models for realistic quantum hardware
- Advanced federated algorithms (FedProx, FedAvg+)
- More quantum circuit architectures
- GPU acceleration for simulation

## 📄 License

MIT License - see [LICENSE](LICENSE) file

## 🙏 Acknowledgments

- **IBM Qiskit**: Quantum computing framework
- **Quantum Machine Learning**: Research community
- **Federated Learning**: Privacy-preserving ML paradigm

## 📚 References

1. Qiskit Documentation: https://qiskit.org/
2. Federated Learning: McMahan et al. (2017)
3. Quantum Machine Learning: Schuld & Petruccione (2018)
4. Variational Quantum Algorithms: Cerezo et al. (2021)

## 🐛 Issues & Support

Found a bug or have questions?
- Open an issue: [GitHub Issues](https://github.com/yourusername/quantum-federated-learning/issues)
- Discussions: [GitHub Discussions](https://github.com/yourusername/quantum-federated-learning/discussions)

## ⭐ Star History

If you find this project useful, please consider giving it a star! ⭐

---

**Built with ❤️ for the quantum + ML community**
```

---

## **Additional Files to Include:**

### **.gitignore**
```
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
env/
venv/
*.egg-info/
dist/
build/

# IDE
.vscode/
.idea/
*.swp
*.swo

# OS
.DS_Store
Thumbs.db

# Results
results/
*.csv
*.png
```

### **requirements.txt**
```
numpy>=1.21.0
matplotlib>=3.5.0
pandas>=1.3.0
qiskit>=1.0.0
qiskit-aer>=0.13.0
```

### **LICENSE** (MIT License example)
```
MIT License

Copyright (c) 2024 [Abina Evenjalin]

Permission is hereby granted, free of charge, to any person obtaining a copy...
```

---

## **GitHub Topics to Add:**
```
quantum-computing
federated-learning
machine-learning
qiskit
quantum-machine-learning
privacy-preserving-ml
hybrid-quantum-classical
variational-quantum-circuits
nisq
python
tkinter
quantum-algorithms
