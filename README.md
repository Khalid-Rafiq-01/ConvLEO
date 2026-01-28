# ConvLEO (LEO): Wind-Conditioned Plume Forecasting

ConvLEO is a convolutional Latent Evolution Operator (LEO) model for wind-conditioned spatiotemporal plume prediction.

**Core idea:** given a single plume observation u(x, y, t) and conditioning (U, θ), predict the future state u(x, y, t+τ) **in one shot** (no autoregressive rollout), where τ is a user-specified time jump.

## Contents
- `ConvLEO.pdf` — overview of the problem, model philosophy, and initial results.

## Problem setup
- **Inputs:** observed plume field u(x, y, t), wind speed U, wind direction θ, and time jump τ.
- **Output:** predicted plume field u_hat(x, y, t+τ).
- **Conditioning vector:** ζ = [U, sin(θ), cos(θ), τ].

## Notes / Roadmap
- Current results focus on **2D** wind-conditioned plume dynamics.
- Next steps: extend to **3D volumetric** plume evolution and extract **iso-surfaces / iso-contours** as post-processing outputs.
- Extension: full-field prediction from **partial observations** (sparse sensors measuring concentration).
- Extension: **bidirectional** ConvLEO for inverse mapping.

## Author
Khalid Rafiq
