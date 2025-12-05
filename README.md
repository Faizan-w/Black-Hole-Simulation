# Black-Hole-Simulation
This project explores whether physics-informed neural networks (PINNs) can accurately approximate spacetime curvature and geodesic motion near a Schwarzschild balck hole, and how their performance compares to traditional numerical relativity solvers

# Research Question
How accurately can physics-informed neural networks (PINNs) approximate geodesic trajectories near a Schwarzschild black hole compared to traditional numerical integration methods?

# Project goals
- Implement the Schwarzschild metric and derive geodesic equations.
- Build a classical numerical solver for ground truth geodesics
- Train a PINN model to satisfy the geodesic equations and conserved quantities.
- Compare PINN trajectories to numerical solutions using:
-   Mean trajectory error
-   Angular deviation
-   Stability near the photon sphere
-   Training efficiency
- Identify condition where PINNs outperform or fail relative to classical integrators

# Background
General relativity predicts that objects follow geodesics, the shortest path between 2 points on a surface, through curved spacetime. Near black holes, curvature becomes extreme, making numerical solutions challenging. 

Tradiitional methods use ODE integration, but they can become unstable near the event horizion, the photon sphere, or other highly eccentric or plunging orbits.

PINNs incorporate physical laws, such as Einsteins equations and geodesic ODEs, directly into the loss function, offering a promising alternative for solving stiff or highly nonlinear differential equations.

# Methods
1. Derivation of Geodesic Equations
   - Start from the Schwarzschild metric
   - Compute Christoffel symbols
   - Derive geodesic ODEs
   - Reduce to equatorial plane
2. Numerical Integration
   - Implement RK4 and adaptive RK solvers
   - Generate benckmark trajectories:
   -   Circular orbits
   -   Bound elliptic orbits
   -   Photon sphere
   -   Plunge trajectories
   - Record positions, velocities, and conserved quantites
3. PINN Training
   - Neural network with MLP architecture
   - Loss = geodesic residuals + metric constraints + conserved quantity penalties
   - Domain sampling near horizon and far from horizon
   - Train until convergence
4. Evaluation Metrics
   - Trajectory RMS error
   - Phase error
   - Stability window
   - Comparison near critical radii like Schwarschild radius and photon sphere

# Results (to be added)

# References

# License
MIT License
   

