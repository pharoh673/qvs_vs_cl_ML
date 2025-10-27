🎓 Quantum vs Classical Classifier — Mini QML Project
🧠 Overview

This project compares a Variational Quantum Classifier (VQC) built with Qiskit Machine Learning to a classical Logistic Regression model from scikit-learn, using synthetic circular data to test performance on a non-linear classification task.
The goal was to understand how quantum feature mapping and entanglement can outperform linear classical models on complex boundaries.

⚗️ Project Objectives

Build and train a VQC using quantum circuits (feature map + ansatz).

Compare against a classical baseline trained on the same dataset.

Visualize decision boundaries and accuracies for both.

Learn practical steps in Quantum Machine Learning (QML) using Qiskit.

🧩 Dataset

Two synthetic datasets were generated:

Unbalanced Dataset: circle with 39% positive samples

Classical accuracy: 0.60

Quantum accuracy: 0.675

Balanced Dataset: 50/50 class distribution

Classical accuracy: 0.394

Quantum accuracy: 0.706

Each dataset contained 2D points labeled by whether they fall inside or outside a circle — a classic non-linear boundary problem.

⚙️ Technologies Used
Category	Libraries / Tools
Quantum ML	Qiskit, Qiskit Aer, Qiskit Machine Learning, Qiskit Algorithms
Classical ML	Scikit-learn
Visualization	Matplotlib, Seaborn
Environment	Python 3.10+, JupyterLab
Results

The Variational Quantum Classifier (VQC) consistently outperformed the classical Logistic Regression baseline:

Dataset	Classical (LogReg)	Quantum (VQC)
Unbalanced	0.60	0.675
Balanced	0.394	0.706

import matplotlib.pyplot as plt

models = ["Classical (LogReg)", "Quantum (VQC)"]
accuracies = [0.394, 0.706]

plt.figure(figsize=(6,4))
bars = plt.bar(models, accuracies, color=["#d95f02", "#1b9e77"], alpha=0.8)
plt.ylim(0.3, 0.85)
plt.ylabel("Accuracy")
plt.title("Classical vs Quantum Classifier Accuracy")

for bar, acc in zip(bars, accuracies):
    plt.text(bar.get_x() + bar.get_width()/2, acc + 0.02, f"{acc:.3f}", ha="center", fontsize=11)
plt.grid(axis="y", linestyle="--", alpha=0.5)
plt.show()

python -m venv qml_env
source qml_env/bin/activate  # (Windows: qml_env\Scripts\activate)
pip install jupyterlab numpy matplotlib seaborn scikit-learn
pip install qiskit qiskit-aer qiskit-machine-learning qiskit-algorithms

Key Takeaways

Quantum models excel when data has non-linear, entangled relationships.

Even a 2-qubit VQC can outperform classical baselines on small datasets.

QML offers a bridge between quantum physics and data science, demonstrating real computational advantages in expressive modeling.

Author

Farhad Amanollahi
Graduate Student in Quantum Physics | Exploring Machine Learning Applications
