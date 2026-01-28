# ConvLEO (LEO): Wind-Conditioned Plume Forecasting

ConvLEO is a **convolutional Latent Evolution Operator (LEO)** model for wind-conditioned spatiotemporal plume prediction.

**Core idea:** given a single plume observation \(u(x, y, t)\) and conditioning \((U,\theta)\), predict the future state \(u(x, y, t+\tau)\) **in one shot** (no autoregressive rollout), where \(\tau\) is a user-specified time jump.

## Contents
- `ConvLEO.pdf` — overview of the problem, model philosophy, and initial results.

## Problem setup
- Inputs: observed plume field \(u(x, y, t)\), wind speed \(U\), wind direction \(\theta\), and time jump \(\tau\).
- Output: predicted plume field \(\hat{u}(t+\tau)\).
- Conditioning vector: \(\zeta=[U,\sin\theta,\cos\theta,\tau]\).

## Notes / Roadmap
- Current results focus on **2D wind-conditioned plume dynamics**.
- Next steps include extending to **3D volumetric plume evolution** and extracting **iso-surfaces / iso-contours** as post-processing outputs.
- Full 2D/Volumetric predictions given partial observations(partial sensors measuring concentration).
- Implementing Bidirectional ConvLEO for solving inverse mapping.

- ## Author
- Khalid Rafiq
