### **1D Burgers Equation Solvers: FDM, PINN, and iPINN**

This repository demonstrates and compares three different approaches to solving the one-dimensional (1D) Burgers equation—a classic nonlinear partial differential equation (PDE) widely used in fluid dynamics and nonlinear wave modeling.



###### \## Featured methods:



**-Finite Difference Method (FDM):** A standard numerical PDE solver, serving as a reference solution.



**-Physics-Informed Neural Networks (PINNs**): A deep learning-based approach that enforces the governing PDE and boundary/initial conditions as soft constraints during training.



**-Inverse Physics-Informed Neural Networks (iPINNs**): Extends PINNs to learn not just the solution but also unknown physical parameters (e.g., viscosity) directly from sparse or noisy observations.



###### \## Motivation

$$

\\frac{\\partial u}{\\partial t} + u \\frac{\\partial u}{\\partial x} = \\nu \\frac{\\partial^2 u}{\\partial x^2}

$$



where \\( u(x, t) \\) is the solution and \\( \\nu \\) is the viscosity.

&nbsp;

is a prototypical nonlinear PDE. Comparing classical solvers (FDM) and neural PDE solvers (PINN/iPINN) helps you:



\-Understand the strengths and limitations of data-driven and traditional approaches.



\-See how PINNs can approximate the solution across the whole domain, not just on a fixed grid.



\-Explore how iPINNs recover both the underlying physics and unknown parameters using limited data—crucial for scientific machine learning and “learning physics from data.”



>The analytical solution for the chosen initial and boundary conditions is:



$$

u(x, t) = -\\sin(\\pi x)\\, \\exp\\big(-\\pi^2 \\nu t\\big)

$$​





###### \## Repository Contents

**fdm\_1d\_burgers.py**: Classical FDM code for time-stepping the 1D Burgers equation, with visualization of solution evolution.



**pinns\_1d\_burgers.py**: PyTorch-based PINN code for learning the solution u(x,t) by minimizing PDE, boundary, and initial condition losses.



**ipinns\_1d\_burgers.py**: PyTorch-based iPINN code that simultaneously learns the solution and the (unknown) viscosity ν using sparse observations and physics constraints.



Each script is self-contained and can be run independently.

## What You’ll Learn

->The accuracy and limitations of PINNs and iPINNs compared to classical methods.



->How PINNs interpolate and generalize in the spatiotemporal domain.



->The power of iPINNs for parameter discovery when traditional measurements are incomplete.



->Visualization of solution evolution and neural PDE solver convergence.



###### \## Extending This Project

\-Try different initial or boundary conditions.



\-Experiment with higher noise or sparser observations for iPINNs.



\-Investigate 2D or system extensions (e.g., Navier-Stokes, Allen–Cahn).



\-Integrate advanced neural architectures (ResNets, Fourier features, etc.) for PINNs.



**License**

This project is licensed under the MIT License.

Feel free to use, adapt, and cite!

