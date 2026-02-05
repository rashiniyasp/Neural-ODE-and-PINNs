# Engineering Analytics – Neural ODEs and Physics-Informed Neural Networks (PINNs)

**Name:** Rashi Niyas  
**Course:** Z6003 – Engineering Analytics, IIT Madras  

---

## Overview

This repository contains the solutions for the assignment of the **Z6003 – Engineering Analytics** course. The assignment explores two advanced neural network paradigms that incorporate continuous dynamics and physical constraints:

1. **Physics-Informed Neural Networks (PINNs):**  
   Applied to solve the *Eikonal equation* for cardiac activation mapping, demonstrating how embedding physical laws into the learning process improves prediction accuracy under sparse data conditions.

2. **Neural Ordinary Differential Equations (Neural ODEs):**  
   Used to model a continuous-depth neural network for a classification task and compared against a standard feedforward neural network in terms of decision boundary smoothness.

---

## Repository Structure

```

Neural-ODE-and-PINNs/
│
├── README.md
├── src/
│   ├── pinns_ea.ipynb        # PINN solution (Eikonal equation)
│   └── node_ea.ipynb         # Neural ODE classification task
└── Results/
├── Node_res.png
├── PINNs_res.png

```

---

## Results and Visualizations

### Neural ODE vs Baseline Neural Network

The figure below compares the **decision boundaries** learned by a baseline neural network and a **Neural ODE** model for a 2D classification task.

- The baseline model exhibits sharper, piecewise decision boundaries.
- The Neural ODE produces smoother and more continuous boundaries due to its continuous-depth formulation.

<p align="center">
  <img src="Results/Node_res.png" width="90%">
</p>

**Figure 1:** Decision boundary comparison between a baseline neural network (left) and a Neural ODE model (right).

---

### Physics-Informed Neural Network (PINN): Cardiac Activation Mapping

The following figure presents:
- Ground truth activation time map \( T(x, y) \)
- Prediction from a purely data-driven neural network
- Prediction from a Physics-Informed Neural Network (PINN)
- Absolute error maps for both approaches

The PINN incorporates the governing **Eikonal equation** as a physics-based constraint, resulting in reduced prediction error and improved physical consistency.

<p align="center">
  <img src="Results/PINNs_res.png" width="90%">
</p>

**Figure 2:** Comparison of ground truth, data-driven model prediction, PINN prediction, and corresponding absolute error maps.

---

## Key Observations

- Neural ODEs learn smoother decision boundaries compared to standard feedforward networks.
- PINNs outperform purely data-driven models when training data is sparse.
- Incorporating physical laws improves generalization, stability, and interpretability.

---

## Conclusion

This assignment demonstrates the effectiveness of **Neural Ordinary Differential Equations** and **Physics-Informed Neural Networks** for engineering problems involving continuous dynamics and physical constraints. Both approaches show clear advantages over traditional neural networks in terms of performance and interpretability.

---
