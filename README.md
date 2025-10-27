# 🎓 Quantum vs Classical Classifier — Mini Quantum Machine Learning Project

### 🧠 Overview
This project compares a **Variational Quantum Classifier (VQC)** built with **Qiskit Machine Learning** to a **classical Logistic Regression** model from **scikit-learn**, using a synthetic circular dataset to test performance on a non-linear classification task.  
The goal was to explore how **quantum feature mapping and entanglement** can outperform classical linear models in detecting non-linear patterns.

---

## ⚗️ Project Objectives
- Build and train a **VQC** using quantum circuits (feature map + ansatz).  
- Compare it with a **classical baseline** (Logistic Regression).  
- Visualize decision boundaries and performance results.  
- Gain practical experience with **Quantum Machine Learning (QML)** using Qiskit.

---

## 🧩 Dataset
Two synthetic datasets were generated and used:

| Dataset | Description | Classical Accuracy | Quantum Accuracy |
|----------|--------------|--------------------|------------------|
| **Unbalanced** | Circle with 39% positive samples | 0.600 | 0.675 |
| **Balanced** | 50/50 class distribution | 0.394 | 0.706 |

Each dataset consisted of 2D points labeled based on whether they fall inside or outside a circle, creating a **non-linear** decision boundary — a task where quantum models shine.

---

## ⚙️ Technologies Used
| Category | Libraries / Tools |
|-----------|------------------|
| **Quantum ML** | Qiskit, Qiskit Aer, Qiskit Machine Learning, Qiskit Algorithms |
| **Classical ML** | Scikit-learn |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Python 3.10+, JupyterLab |

---

## 📈 Results
The **Variational Quantum Classifier (VQC)** consistently outperformed the **classical Logistic Regression** baseline.

| Dataset | Classical (LogReg) | Quantum (VQC) |
|----------|--------------------|---------------|
| Unbalanced | 0.60 | 0.675 |
| Balanced | 0.394 | 0.706 |

Quantum circuits leverage **quantum feature maps** and **entanglement** to embed data into higher-dimensional quantum state spaces, enabling the model to capture complex non-linear structures that classical models cannot.

---

## 📊 Example Comparison Plot

```python
import matplotlib.pyplot as plt

models = ["Classical (LogReg)", "Quantum (VQC)"]
accuracies = [0.394, 0.706]

plt.figure(figsize=(6,4))
bars = plt.bar(models, accuracies, color=["#d95f02", "#1b9e77"], alpha=0.8)
plt.ylim(0.3, 0.85)
plt.ylabel("Accuracy")
plt.title("Classical vs Quantum Classifier Accuracy")

for bar, acc in zip(bars, accuracies):
    plt.text(bar.get_x() + bar.get_width()/2, acc + 0.02, f"{acc:.3f}", 
             ha="center", fontsize=11)
plt.grid(axis="y", linestyle="--", alpha=0.5)
plt.show()
