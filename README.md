# Deep Learning-Based Medical Image Analysis for Breast Ultrasound

This project explores deep learning methods for **breast ultrasound image analysis** using the BUSI dataset.

## Project Goals

* Breast lesion **classification**
* Lesion **segmentation**
* Model **explainability** using Grad-CAM
* Comparison between **full-image** and **lesion ROI** classification

## Dataset

**BUSI (Breast Ultrasound Images Dataset)**

The dataset contains:

* Benign
* Malignant

images, with segmentation masks available for lesion images.

## Current Pipeline

1. **Dataset Quality Control**

   * Checked image/mask pairs
   * Checked image dimensions and validity
   * Checked duplicates and corrupted files

2. **Dataset Splitting**

   * Train: 70%
   * Validation: 15%
   * Test: 15%

3. **Classification Baseline**

   * ResNet50
   * 2-class classification:

     * Benign
     * Malignant

4. **Lesion Segmentation**

   * U-Net
   * Binary lesion segmentation

5. **ROI Classification**

   * U-Net predicted masks are used to extract lesion ROIs
   * ResNet50 classifies:

     * Benign
     * Malignant

6. **Explainability**

   * Grad-CAM will be used to visualize regions influencing classification.

## Models

* **ResNet50** — image classification
* **U-Net** — lesion segmentation
* **Grad-CAM** — model interpretation

## Evaluation

Classification:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix

Segmentation:

* Dice coefficient
* IoU

## Project Status

* [x] Dataset inspection
* [x] Dataset split
* [x] Full-image classification baseline
* [x] U-Net segmentation
* [ ] Predicted ROI generation
* [ ] ROI classification
* [ ] Grad-CAM analysis
* [ ] Final comparison and analysis

## Notes

This README is a temporary project overview and will be updated as the experiments and analysis are finalized.
