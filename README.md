
# Text Classification Template

This is a text classification template using `imdb` dataset from HuggingFace datasets and training is powered by PyTorch and PyTorch-Ignite.

## Getting Started

Install the dependencies with `pip`:

```sh
pip install -r requirements.txt --progress-bar off -U
```

## Training

The training consider a deterministic process, all the training state (models, optimizers, trainers, ...) will be saved in the logs using TensorBoard tracking system. The best metric scored model will be the saved one.

It's important to mention that the training will be stoped if there is Inf/NaN tensors found. We also have added a number of events to wait if no improvement is verified and then stop the training (6x).

### 1 GPU Training

```sh
python main.py
```
