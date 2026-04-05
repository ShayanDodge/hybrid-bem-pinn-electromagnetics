# BEM-PINN Framework for Laplace Equation on L-Shaped Domains

This repository contains implementations of a coupled **Boundary Element Method (BEM)** and **Physics-Informed Neural Network (PINN)** framework for solving the **Laplace equation** on L-shaped domains.

The project is organized into versioned implementations, progressing from a baseline model to more advanced physical configurations.

---

## 📌 Versions

### 🔹 v1.0.0 — Homogeneous L-Shaped Domain
**Folder:** `Homogeneous L-Shaped Domain (V1.0.0)`

- Baseline implementation of the BEM-PINN framework  
- Solves the Laplace equation on a homogeneous L-shaped domain  
- Domain decomposition:
  - Left subdomain → solved using PINN  
  - Right-bottom subdomain → solved using BEM  
- Coupling enforced through interface boundary conditions  

👉 This version establishes the core methodology and validates the approach.

---

### 🔹 v1.1.0 — Non-Homogeneous L-Shaped Domain *(Coming Soon)*
- Extension to non-homogeneous / multi-material domains  
- Incorporates interface conditions between different materials  
- Improved physical realism and modeling capability  

🚧 This version is currently under development and will be released soon.

---

## 🧠 Method Overview

The general workflow across versions:

1. Construct the L-shaped computational domain  
2. Define Dirichlet and Neumann boundary conditions  
3. Train a PINN on one subdomain  
4. Use PINN predictions at the interface  
5. Solve the complementary subdomain using BEM  
6. Reconstruct the global solution  

---

## 🛠 Requirements

- MATLAB  
- Deep Learning Toolbox  
- Optimization Toolbox  
- Parallel Computing Toolbox  

---

## 🚀 Getting Started

1. Open MATLAB  
2. Navigate to a version folder (e.g., `V1.0.0`)  
3. Run the main script inside the `main/` directory  

Example command:

run_bem_pinn_laplace_lshape

---

## 📊 Output

Each version produces:

- Scalar potential field  
- Gradient fields  
- BEM reconstruction  
- Combined contour visualization  

---

## 📄 Related Paper

**Solving Laplace Equations with a Combined BEM and PINN Approach**

(Add full IEEE citation here)

---

## 📚 Citation

If you use this work, please cite:

```bibtex id="sc0yz4"
@article{yourpaper,
  title={Solving Laplace Equations with a Combined BEM and PINN Approach},
  author={Author Name(s)},
  journal={Journal Name},
  year={2024}
}
