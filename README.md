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
