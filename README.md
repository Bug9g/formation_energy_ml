# Formation Energy Prediction with Machine Learning Potentials

This repository contains code and experiments for my course project at HSE University,
where I compare two machine learning models — **MatterSimV1** and **EquiformerV2** —
on the task of predicting formation energies of hydrocarbons.

---

## Repository Structure
- `notebooks/` — Kaggle notebooks used for training and evaluation:
  - `mattersim_training.ipynb`
  - `equiformer_training.ipynb`
- `src/` — helper scripts (custom dataset parser, training utilities)
- `results/` — training logs, plots, and evaluation metrics
- `data/` — instructions for dataset preparation (not uploaded due to size)

---

## Dataset
- Hydrocarbon dataset in `.xyz` format  
- Each structure has associated **U₀ energy** values  
- The dataset is split into train/val/test subsets  

*(Note: raw data is not included due to size restrictions. Instructions for dataset preparation are in `data/README.md`.)*

---

## Models
- **MatterSimV1** — fine-tuned on hydrocarbon dataset
- **EquiformerV2** — fine-tuned on the same dataset

---

## Results
| Model        | MAE (eV/atom) | Notes                |
|--------------|---------------|----------------------|
| MatterSimV1    | 0.0016        | evaluated on validation subset |
| EquiformerV2 | 0.1185        | evaluated on train subset (training stopped early due to memory limits) |

*(To be updated as experiments progress.)*

---

### Limitations
- Training **EquiformerV2** on full dataset was not completed because of **memory limitations**.  
- All experiments were run on **Kaggle free GPUs (16GB Tesla T4)** and locally on **MacBook Air M4 (CPU only)**.  
- Results for EquiformerV2 should be considered preliminary.

--- 

## ⚙️ Requirements
Install dependencies from `requirements.txt`:
