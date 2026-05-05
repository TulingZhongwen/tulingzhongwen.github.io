```markdown
# Inertia-Tension Theory (ITT) – Consciousness Measurement Toolkit

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19533323.svg)](https://doi.org/10.5281/zenodo.19533323)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Author:** Tuling Zhongwen (图灵中文)

This repository provides a reproducible implementation of the **Inertia‑Tension Theory (ITT)**, a first‑principles physical theory of consciousness. ITT defines two core quantities – **causal loop strength Λ** and **accessible self‑distance Θ(s)** – and three testable predictions that can be evaluated using resting‑state EEG/fMRI data.

## 🔬 Three Core Predictions

1. **Consciousness emergence**: In awake states, Λ significantly exceeds the shuffled‑data baseline (`Λ > Λ_noise`); under deep sleep or anaesthesia, Λ is not significantly different from noise.
2. **Degree of consciousness**: The mean Θ(s) decreases across awake → drowsy → anaesthetised (Cohen's d > 0.8).
3. **Self‑force direction rule**: The sign of the dot product `Δ̅·∇U` predicts the direction of spontaneous state change (agreement >75% in a binomial test).

## 📦 Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/YOUR_USERNAME/ITT-experiment.git
cd ITT-experiment
pip install -r requirements.txt
```

Dependencies: numpy, scipy, scikit‑learn, mne (for EEG), matplotlib, nolds (optional), antropy (optional).

🚀 Quick start (with simulated chaotic data)

The example_lorenz.py (or example_lorenz.ipynb) demonstrates the pipeline:

· Reconstruct state space from a time series (Takens embedding).
· Estimate local Jacobian matrices and compute Λ.
· Compare Λ with Λ_noise via permutation test.
· Compute accessible self‑distance Θ(s).

Run the example:

```bash
python example_lorenz.py
```

Expected output:

· Lorenz system: Λ >> Λ_noise (p < 0.01)
· White noise: Λ ≈ Λ_noise (p > 0.05)

📊 Real‑world data (EEG/fMRI)

The code can be adapted to any time series. We suggest starting with public datasets:

· OpenNeuro ds003478 (awake‑sleep EEG)
· Human Connectome Project (resting‑state fMRI)
· OpenNeuro ds002718 (propofol sedation)

Example notebooks for these datasets will be added incrementally.

📜 Theory reference

The full mathematical derivation, postulates and falsification conditions are available in the ITT version 5 paper:

Tuling Zhongwen (图灵中文). (2026). Inertia‑Tension Theory (ITT) version 5: A first‑principle theory of consciousness (final consciousness edition). Zenodo.
DOI: 10.5281/zenodo.19533323

🤝 Contributing

Issues, pull requests, and independent re‑implementations are welcome. Please adhere to the MIT license and cite the Zenodo record.

📝 Citation

If you use this code or ITT in your research, please cite both the Zenodo paper and this software:

```bibtex
@software{TulingZhongwen_ITT_Experiment_2026,
  author       = {Tuling Zhongwen (图灵中文)},
  title        = {ITT-experiment: Implementation of the Inertia‑Tension Theory for consciousness measurement},
  year         = {2026},
  publisher    = {GitHub},
  url          = {https://github.com/YOUR_USERNAME/ITT-experiment},
  doi          = {10.5281/zenodo.19533323}   % replace with Zenodo DOI after first release
}
```

📄 License

Distributed under the MIT License. See LICENSE for more information.

---
