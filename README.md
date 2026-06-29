# CNN on Sign Language

PyTorch convolutional neural network for classifying hand-sign images from the Sign Language MNIST dataset.

This project demonstrates an end-to-end computer-vision training pipeline: dataset download, preprocessing, custom `Dataset`, `DataLoader`, CNN architecture, training loop, validation loop, and model evaluation.

## Project Overview

The notebook trains a CNN on grayscale 28x28 sign-language images. The saved run reaches about 97% validation accuracy, while also showing practical model-building choices such as normalization, convolutional layers, batch normalization, dropout, and cross-entropy loss.

## Dataset

Dataset source:

- `datamunge/sign-language-mnist` through `kagglehub`

The dataset contains image pixels in CSV format. The notebook reshapes each row into a `1 x 28 x 28` image tensor and normalizes pixel values by dividing by 255.

## Model Architecture

The CNN uses:

- `Conv2d` layers for spatial feature extraction.
- `BatchNorm2d` for training stability.
- `ReLU` activations.
- `MaxPool2d` for downsampling.
- `Dropout` to reduce overfitting.
- Fully connected layers for 24-class classification.

## Repository Structure

| File | Purpose |
|---|---|
| `CNN_on_Sign_Language_MNIST.ipynb` | Full notebook for downloading data, building the dataset pipeline, defining the CNN, training, and validation. |

## Tech Stack

- Python
- PyTorch
- pandas
- KaggleHub
- Jupyter Notebook

## How To Run

1. Clone the repository:

```bash
git clone https://github.com/yg36/CNN-on-Sign-Language.git
cd CNN-on-Sign-Language
```

2. Create and activate a virtual environment:

```bash
python -m venv .venv
```

Windows:

```bash
.venv\Scripts\activate
```

macOS/Linux:

```bash
source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Open the notebook:

```bash
jupyter notebook CNN_on_Sign_Language_MNIST.ipynb
```

5. Run the notebook cells in order.

## Results From Saved Run

- Training accuracy reaches nearly 100% in later epochs.
- Validation accuracy remains around 96-97% across later epochs.
- Final saved epoch shows validation accuracy around 97.2%.

## Recruiter-Relevant Signal

This repo shows practical computer-vision implementation in PyTorch: image preprocessing, custom datasets, dataloaders, CNN design, validation logic, and classification evaluation. It is a stronger AI/ML portfolio signal than a basic notebook because it covers the actual training pipeline.

<!-- repository-refresh: 2026-06-29 | preserved-order-rank: 002/71 -->
