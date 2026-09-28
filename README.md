# Indian Sign Language Recognition

Image preprocessing and CNN/transfer-learning experiments for classifying isolated hand-sign images.

[Architecture notebook](notebooks/architecture-comparison.ipynb) · [Original report](docs/report.pdf)

## Data and environment

The original notebook uses Google Colab and a private Google Drive folder named `Indian`, with one subdirectory per class. The dataset is not redistributed here. Review the report for the original experiment context and obtain the matching dataset with permission before running it.

Dependencies include TensorFlow/Keras, OpenCV, NumPy, pandas, seaborn, matplotlib, and scikit-learn. Update the notebook's Drive paths to your own dataset and checkpoint locations. Legacy Keras APIs may require adaptation.

## Evaluation

The initial CNN example now separates training, validation, and final test data. Validation is used during fitting; the held-out test is used only for final evaluation. Later transfer-learning sections use their own split and should not be treated as directly comparable until the same examples and preprocessing are used across models.

Where multiple images come from the same signer or recording, use signer/session-level separation before reporting generalization. No new accuracy is claimed; the revised cells need rerunning with the original data.

## Scope

This classifies isolated signs in the available images. It does not implement continuous sign-language translation. Pretrained architectures and libraries retain their upstream attribution.
