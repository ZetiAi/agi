# AGI

A from-scratch GPT-style Transformer (PyTorch) aimed at understanding, writing and explaining code, starting with Python.

## Deployment map

**Status:** archived to the HDD 2026-10-06. never deployed. Research training code, dormant since 2024-10.

```text
Colab GPU notebook (agi.ipynb clones this repo) → PyTorch Lightning + DeepSpeed stage 2 → checkpoints, hparams, TensorBoard logs → Google Cloud Storage
```

| Layer | Platform | Notes |
|---|---|---|
| Compute | Google Colab GPU runtime | Falls back to CPU locally. CLI: `poetry run python src/main.py` with encode, train or predict |
| Storage | Google Cloud Storage (google-cloud-storage) | Service-account auth via GOOGLE_APPLICATION_CREDENTIALS; bucket set in config.yaml |
| Tracking | Weights & Biases, TensorBoard | |
| CI/CD | none | Dependabot only |

_Mapped 2026-10-04 from the default branch's config. Update this section when a platform changes._
