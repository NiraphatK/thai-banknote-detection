# Thai Banknote Detection with YOLOv8

An object-detection project for recognizing **Thai Baht banknotes** using Ultralytics YOLOv8.

The project focuses on building a labeled image dataset for five Thai banknote denominations and using it for model training and inference experiments in Google Colab.

## Supported banknote classes

The repository organizes images for these denominations:

- 20 Baht
- 50 Baht
- 100 Baht
- 500 Baht
- 1,000 Baht

## Project goals

- Collect and organize Thai banknote images by denomination
- Prepare object-detection annotations in YOLO format
- Train a YOLOv8 detector on the custom dataset
- Evaluate the model through test images and inference experiments
- Provide a Colab-based workflow so training can run without a local GPU setup

## Tech stack

| Area | Technology |
| --- | --- |
| Model | Ultralytics YOLOv8 |
| Task | Object detection |
| Annotation | LabelImg / YOLO format |
| Experiment environment | Google Colab |
| Data preparation | Python / Jupyter Notebook |

## Repository structure

```text
thai-bank-detection/
├── twentyBaht/          # Images for 20 Baht banknotes
├── fiftyBaht/           # Images for 50 Baht banknotes
├── hundredBaht/         # Images for 100 Baht banknotes
├── fiveHundredBaht/     # Images for 500 Baht banknotes
├── thousandBaht/        # Images for 1,000 Baht banknotes
├── download_image.ipynb # Image/data preparation notebook
└── README.md
```

## Workflow

A typical training workflow for this project is:

1. Collect banknote images.
2. Organize the images by denomination.
3. Annotate banknotes with bounding boxes using LabelImg.
4. Export annotations in YOLO format.
5. Prepare the dataset configuration required by YOLOv8.
6. Train the detector in Google Colab.
7. Run inference against unseen images and inspect detections.

## Train and experiment in Google Colab

The project includes a Colab workspace for the training/testing workflow:

[Open the project in Google Colab](https://colab.research.google.com/drive/1Aeq77SH6MFBccXbQGgADBObeWNJhKglU?usp=sharing)

## Dataset notes

The repository contains denomination-specific image directories used during dataset preparation. Depending on the experiment, annotations and train/validation splits may be generated or managed within the Colab workflow rather than committed as a finalized standalone dataset package.

## Model evaluation

This repository currently does not publish a canonical accuracy, precision/recall, or mAP result in the README. Model quality should therefore be assessed from the training run being used rather than assuming a fixed benchmark.

When a stable model is selected, useful additions here would include:

- Dataset size and train/validation split
- YOLOv8 model variant used
- Training epochs and image size
- Precision, recall, mAP@0.5, and mAP@0.5:0.95
- Example detection outputs

## Background

This project was developed as part of an Artificial Intelligence course and demonstrates the end-to-end workflow of preparing a custom dataset and applying modern object detection to a locally relevant recognition problem.

## Status

Academic / experimental project. The repository is useful as a dataset-preparation and YOLOv8 learning reference, but it should not be treated as a production-grade currency recognition or financial verification system.