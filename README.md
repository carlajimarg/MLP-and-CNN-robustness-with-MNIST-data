# MNIST Robustness

A PyTorch experiment comparing an MLP and a CNN on MNIST, focusing on how their performance changes under rotation, Gaussian noise and translation.

The notebook also tests whether data augmentation can improve robustness.

## Results before augmentation

| Test | MLP | CNN |
|---|---:|---:|
| Clean | 97.48% | 98.74% |
| Rotate 20° | 91.07% | 94.33% |
| Gaussian noise | 93.27% | 93.24% |
| Shift 4 px | 6.88% | 16.97% |

Both models perform well on clean MNIST, but their accuracy drops under image transformations, especially translation.

## Results after augmentation

| Test | MLP | CNN |
|---|---:|---:|
| Clean | 97.82% | 99.01% |
| Rotate 20° | 92.31% | 95.40% |
| Gaussian noise | 95.88% | 97.46% |
| Shift 4 px | 49.43% | 72.98% |

Data augmentation improves robustness across all tested transformations, with the largest improvement on shifted images.

## Run

```bash
pip install -r requirements.txt
jupyter notebook
```
