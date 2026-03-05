# 3D Imperative A* (iAstar3D)

This repository contains the 3D path planning algorithm based on Differentiable A* and its application to multi-agent formation control.

## Project Structure

- `core/`: Core algorithm implementations (`iastar3d.py`, `dastar3d.py`, `encoder3d.py`).
- `data/`: Dataset generation and loading scripts.
- `scripts/`: Training and evaluation scripts.
- `example/`: Application examples (e.g., 3D multi-agent formation control).
- `config/`: Configuration files for training and evaluation.
- `model/`: Pre-trained model weights (please place your `.pkl` files here).

## Quick Start

### 1. Generate Dataset
```bash
python data/generate_3d_dataset.py --out planning-datasets-3d --n_train 800 --n_val 100 --n_test 100
```

### 2. Train the Model
```bash
python scripts/train3d.py
```

### 3. Evaluate the Model
```bash
python scripts/evaluate3d.py
```

### 4. Run the Formation Control Example
Make sure you have a trained model checkpoint in the `model/` directory.
```bash
python example/formation_iastar_3d.py
```
