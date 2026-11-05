# Helmet Detection Using CNN

A computer-vision project report exploring helmet detection for road-safety monitoring, with a related discussion of vehicle and license-plate recognition.

## Project overview

The project describes a workflow that takes an image or video frame, preprocesses it, detects a rider/vehicle, and classifies whether the rider is wearing a helmet. The report also discusses a related license-plate recognition (LPR) pipeline using OCR/CRNN-style recognition.

**Project scope documented in the report**
- Helmet / no-helmet classification using a CNN.
- Image and video input as possible sources.
- Image preprocessing such as resizing, normalization, and augmentation.
- Discussion of object-detection approaches such as YOLO or Faster R-CNN.
- Related license-plate detection and character recognition using OCR/CRNN concepts.

## Technologies discussed

- Python 3.7+
- TensorFlow / Keras or PyTorch for deep learning
- OpenCV for image and video processing
- NumPy and Pandas for data handling
- Matplotlib for visualization
- scikit-learn for evaluation
- Tesseract OCR / pytesseract for text recognition

The exact framework, model architecture, dataset, and package versions used in a runnable implementation should be confirmed from the source code before reproducing results.

## Repository contents

```text
Helmet-Detection-CNN/
├── docs/
│   └── Helmet-Detection-Project-Report.pdf
├── screenshots/
│   ├── result-page-28.png
│   ├── result-page-29.png
│   ├── result-page-30.png
│   ├── result-page-31.png
│   └── result-page-32.png
├── .gitignore
├── README.md
└── requirements.txt
```

## Screenshots from the report

The following images are extracted from the result/demo section of the submitted project report. They illustrate the reported application workflow; they are not independent verification of model performance.

### Demo and detection results

![Result page 28](screenshots/result-page-28.png)

![Result page 29](screenshots/result-page-29.png)

![Result page 30](screenshots/result-page-30.png)

![Result page 31](screenshots/result-page-31.png)

![Result page 32](screenshots/result-page-32.png)

## Setup

This repository package currently contains project documentation, the original report, and report screenshots. It does **not** yet include the runnable Python application, training dataset, trained model weights, or a verified inference script.

After adding the actual Python source code, create and activate a virtual environment:

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
```

Tesseract OCR is a separate system application; installing the Python `pytesseract` package alone does not install the Tesseract executable.

## Suggested workflow

1. Collect and label images of riders with helmets and without helmets.
2. Split the dataset into training, validation, and test sets.
3. Resize and normalize images; apply suitable data augmentation.
4. Train and validate a CNN classifier (or an object-detection model if bounding-box detection is required).
5. Evaluate on held-out data using precision, recall, F1-score, and a confusion matrix.
6. Test on images or video that were not used during training.

## Important notes

- The report discusses both helmet detection and license-plate recognition. A working LPR component requires its own detection/OCR implementation and suitable data.
- Do not describe report figures or example metrics as independently reproduced results unless you have run the code and evaluated the model yourself.
- Before making the repository public, review the included PDF for personal details or institutional information you do not want to publish.

## Author / academic context

Prepared as an academic project report for the Department of Computer Science and Engineering, Malla Reddy Engineering College for Women, academic year 2024–2025. Refer to the report in `docs/` for the contributor and guide details.
