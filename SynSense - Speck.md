# sinabs Tutorial

Hands-on notebooks for learning Spiking Neural Networks with [sinabs](https://sinabs.readthedocs.io).

## Notebooks

| Notebook | Description |
|---|---|
| `snn_mnist_tutorial.ipynb` | Core SNN tutorial — IAF neuron, BPTT, surrogate gradients, training on N-MNIST |
| `snn_dvs_gesture_tutorial.ipynb` | Same concepts applied to DVS Gesture — a genuinely temporal task |
| `snn_exercises.ipynb` | Open-ended explorations to deepen your understanding |

Recommended order: N-MNIST tutorial → DVS Gesture tutorial → exercises.

---

## Environment setup (one time)

```bash
conda create -n sinabs_tutorial python=3.10 -y
conda activate sinabs_tutorial
pip install -r requirements.txt
pip install jupyter ipykernel
python -m ipykernel install --user --name sinabs_tutorial --display-name "sinabs_tutorial"
```

**Every time you open a notebook:** select `sinabs_tutorial` as the kernel.
- JupyterLab: kernel selector (top right)
- VS Code: kernel selector (top right) → Python 3.10 (sinabs_tutorial)

---

## DVS Gesture dataset (manual download required)

The DVS Gesture dataset is hosted on figshare, which blocks automated downloads with bot protection. You must download it manually through a browser before running `snn_dvs_gesture_tutorial.ipynb`.

**Step 1 — Download both files in your browser:**
- Train set (~1.3 GB): https://figshare.com/ndownloader/files/38022171 → `ibmGestureTrain.tar.gz`
- Test set (~270 MB): https://figshare.com/ndownloader/files/38020584 → `ibmGestureTest.tar.gz`

**Step 2 — Move and extract (run in terminal from this folder):**

```bash
mkdir -p data/DVSGesture
mv ~/Downloads/ibmGestureTrain.tar.gz data/DVSGesture/
mv ~/Downloads/ibmGestureTest.tar.gz  data/DVSGesture/

cd data/DVSGesture
tar -xzf ibmGestureTrain.tar.gz
tar -xzf ibmGestureTest.tar.gz
```

After extraction you should have `ibmGestureTrain/` and `ibmGestureTest/` folders with hundreds of `.npy` files inside. tonic will detect them automatically and skip the download.

**N-MNIST** (used in `snn_mnist_tutorial.ipynb`) downloads automatically on first run — no manual step needed.

### Requirements.txt

```
sinabs>=1.2
tonic>=1.4
torch>=1.8
torchvision
matplotlib
numpy
```
