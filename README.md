# Q-Sentinel-Towards-Adversarial-Robustness-for-QIC_xApps-in-Intelligent-O-RAN
Open-source drop of Q-Sentinel and Quantum Adversarial Training (QAT) for resilient O-RAN xApp signal classification, pairing a ResNet-18 backbone with PennyLane-driven 6-qubit circuits (quantum_classical_hybrid.py:24).
**Highlights**

- Unified training stack with clean baselines, adversarial fine-tuning, and the full Quantum-Sentinel defense suite (qs_sentinel.py:29).
- Quantum State Transformer, decision-boundary reinforcement loss, and stochastic smoothing defenses for QC-FGSM, QC-PGD, and QC-poison attacks (defense_utils.py:52).
- Reproducible CLI runner that trains, evaluates, and logs robustness metrics plus Hilbert-space drift visualizations (qsentinel_train_eval.py:1, plot_hilbert_drift.py:1).
- Dataset tooling for SOI vs. CWI spectrogram ingestion, balancing, and visualization (data_handler.py:17).
**Get Started**

- Clone the repo, create the conda environment from env.yml, or install with pip install -r requirements.txt.
- Prepare SOI/CWI spectrogram folders and point create_real_data_loaders at them, or drop images into temp_combined_dataset as described in data_handler.py:49.
- Launch experiments: python qsentinel_train_eval.py --epochs 20 --device cuda --out ./reports_qs.
