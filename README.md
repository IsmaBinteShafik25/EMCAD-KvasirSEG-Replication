
# EMCAD Replication on Kvasir-SEG

This repository contains the experimental verification and replication of EMCAD for polyp segmentation using the Kvasir-SEG dataset.

## Paper

EMCAD: Efficient Multi-scale Convolutional Attention Decoder for Medical Image Segmentation


## Experimental Setup

### Environment

- Platform: Kaggle Notebook
- Framework: PyTorch
- GPU: NVIDIA Tesla T4


### Model Configuration

- Encoder: PVTv2-B2
- Decoder: EMCAD
- Task: Binary Polyp Segmentation


### Training Configuration

| Parameter | Value |
|---|---|
| Dataset | Kvasir-SEG |
| Image Size | 352 x 352 |
| Batch Size | 8 |
| Epochs | 5 |
| Optimizer | AdamW |
| Learning Rate | 0.0005 |


## Dataset

Kvasir-SEG dataset organization:

data/polyp/Kvasir-SEG/

train/
- images
- masks

val/
- images
- masks

test/
- images
- masks


Dataset split:

| Split | Images |
|---|---|
| Train | 700 |
| Validation | 150 |
| Test | 150 |


## Results

| Dataset | Dice Score | Parameters | FLOPs |
|---|---|---|---|
| Kvasir-SEG | 0.8866 | 26.76M | 10.58G |


Best Validation Dice:

0.9112


## Qualitative Results

Prediction visualization:

results/qualitative_results.png


## Repository Structure

train_polyp.py

test_polyp.py

lib/

utils/

results/
- run_log.txt
- benchmark_metrics.csv
- qualitative_results.png


## Reproducibility

Training:

python train_polyp.py

Testing:

python test_polyp.py
