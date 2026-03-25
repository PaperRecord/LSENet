# LSENet

A network for small targets in aerial images.

# Installation

Clone repo and create conda environment (recommended).
Then install requirements.txt in a Python>=3.8.0 environment, including PyTorch>=1.8.

```bash
git clone https://github.com/PaperRecord/LSENet.git
cd LSENet
conda create -n LSENet python=3.8
conda activate LSENet
pip install -r requirements.txt
```

# Datasets

Prepare your dataset in the following format and modify the dataset path in `ultralytics/cfg/datasets/your_dataset.yaml`.

```
dataset
--images
  --train
  --val
--labels
  --train
  --val
```

# Training

Most of training configurations can be changed in the "Train settings" section of `ultralytics/cfg/models/hyper-yolo/LSENet.yaml`.
The key factors are model, data, img, epochs, batch, device and training hyperparameters.

```bash
python train.py
```

# Evaluation

Most of evaluation configurations can be changed in the "Val/Test settings" section of `ultralytics/cfg/default.yaml`.

```bash
python val.py
```
