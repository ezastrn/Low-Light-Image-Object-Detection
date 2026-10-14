# Low-Light Image Object Detection

An object-detection experiment for low-light imagery, trained with Ultralytics YOLO. The project prepares image annotations in YOLO format, creates a train/validation split, trains a 12-class detector, and demonstrates inference on sample images.

## Project overview

The experiment targets these classes: Bicycle, Boat, Bottle, Bus, Car, Cat, Chair, Cup, Dog, Motorbike, People, and Table. Training ran for 30 epochs at an image size of 640 pixels using a YOLO small model.

## Repository layout

```text
.
├── assets/
│   └── samples/             # Example images used for inference
├── configs/
│   └── dataset.yaml         # YOLO dataset configuration
├── notebooks/
│   └── training_workflow.ipynb
├── results/
│   └── results.csv          # Per-epoch training and validation metrics
├── .gitignore
├── requirements.txt
└── README.md
```

## Training results

The final epoch reached **mAP@50 of 0.67830** and **mAP@50–95 of 0.43209**. Full per-epoch losses, precision, recall, mAP, validation losses, and learning rates are available in [`results/results.csv`](results/results.csv).

## Notebook workflow

The notebook documents the complete experimental flow:

1. Prepare the low-light image dataset and annotations.
2. Convert annotations into YOLO label files.
3. Split the dataset into training and validation sets.
4. Train the detector.
5. Run inference on the included sample images.

The original training dataset, model weights, and generated run artefacts are intentionally excluded because they are large. The dataset configuration and experiment metrics are included to make the work easy to review and reproduce.
