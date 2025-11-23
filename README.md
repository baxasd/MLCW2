**Project Overview**
- **Name**: Coursework2-ML — Image segmentation/classification experiments
- **Purpose**: Jupyter notebook-based machine learning coursework that trains, evaluates, and predicts image classes/segments using the provided dataset and helper code.

**Main Notebook**
- **File**: `Z22590018_MLCW2.ipynb` — Contains the data exploration, preprocessing, model training, evaluation, and prediction code used for this coursework.

**Repository Layout**
- **Root**: Contains the main notebook `Z22590018_MLCW2.ipynb`.
- **Dataset**: `intel/` contains three subfolders used by the notebook:
  - `seg_train/` — training images, subfolders per class: `buildings/`, `forest/`, `glacier/`, `mountain/`, `sea/`, `street/`.
  - `seg_test/` — test images, same class subfolders.
  - `seg_pred/` — images used for prediction/inference (predictions saved here or read from here).

**Quick Setup**
1. Create a Python virtual environment (recommended Python 3.8+):

```bash
python3 -m venv .venv
source .venv/bin/activate
```

2. Install common ML packages (adapt as needed; check the notebook for exact dependencies):

```bash
pip install --upgrade pip
pip install jupyterlab notebook numpy pandas matplotlib scikit-learn pillow seaborn
# If using TensorFlow/Keras or PyTorch, install one of these depending on notebook code:
pip install tensorflow   # or
pip install torch torchvision torchaudio
```

3. Start Jupyter and open the notebook:

```bash
jupyter lab   # or `jupyter notebook`
```

**How to Run**
- Open `Z22590018_MLCW2.ipynb` in Jupyter.
- Follow the notebook cells in order (data loading → preprocessing → model training → evaluation → prediction).
- Ensure the `intel/` dataset path is available relative to the notebook. If the notebook expects a different path, update the path variables at the top of the notebook accordingly.

**Reproducing Results**
- Use the same random seeds (if set in the notebook) and the same package versions to improve reproducibility.
- If training large models, consider running on a machine with GPU support and installing the GPU-enabled packages of TensorFlow or PyTorch.

**Notes & Tips**
- The exact package versions required may be specified inside the notebook — inspect the first cells for imports and version pins.
- If you want, I can generate a `requirements.txt` with the environment used by the notebook (I can inspect the notebook and produce pinned dependencies).

**Contact / Author**
- Dataset and notebook maintained by the project owner — see the notebook metadata for author info.

**License**
- Check the course or project instructions for license details. No license file is included by default.

---

If you'd like, I can:
- generate a `requirements.txt` by scanning the notebook for imports,
- add example training/evaluation scripts (Python files) to run outside Jupyter, or
- prepare a small `Makefile` or CLI wrapper to run common tasks.

