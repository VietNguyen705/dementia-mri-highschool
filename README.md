# Dementia Prediction from Brain MRI: a Simple CNN

A 10-week summer research project for high school students.

Title: Simple Dementia Prediction from Brain MRI Images Using a Convolutional Neural Network.

Research question: Can a simple CNN classify brain MRI images into four dementia-stage categories (Non-Demented, Very Mild, Mild, Moderate)?

## How to start

1. Open `dementia_mri_classification.ipynb` -- or launch it directly in Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VietNguyen705/dementia-mri-highschool/blob/main/dementia_mri_classification.ipynb)
2. Switch the runtime to GPU (Runtime -> Change runtime type -> T4 GPU).
3. Fill in every TODO cell from top to bottom.


## 10-Week Plan

<table>
  <thead>
    <tr><th>Week</th><th>Tasks</th></tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Understand the problem: learn basic terms (dementia, Alzheimer's, MRI, brain atrophy), read the OASIS overview, and decide your research question. No coding</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Set up Colab/Drive, download the OASIS dataset, count images per class, and check whether the four classes are balanced or imbalanced</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Display sample MRIs from each class. Check image size, color format, and quality. Make a class-distribution chart</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Resize all images to one size (e.g. 128x128). Normalize pixels to 0-1. Split into train/val/test (70/15/15), stratified by class</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Build a simple CNN (Conv + MaxPool x2, Flatten, Dense, softmax). Train it and plot training vs validation accuracy</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Evaluate with accuracy, precision, recall, F1, and a confusion matrix. Note the strongest and weakest classes (recall matters - missing dementia is serious)</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Carefully try 2-3 improvements (dropout, data augmentation, more epochs). Keep a comparison table of model versions</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Add Grad-CAM heatmaps for a few correct and incorrect examples to show where the CNN focused</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Write the IEEE-style paper (abstract, intro, background, methods, results, discussion, limitations, conclusion). Make results figures</td>
    </tr>
    <tr>
      <td>10</td>
      <td>Final paper, slides, and 3-minute oral presentation. Discuss limitations and ethics</td>
    </tr>
  </tbody>
</table>

## Methodology

1. Load MRI images.
2. Resize and normalize images.
3. Split into train, validation, and test sets.
4. Train a simple CNN.
5. Evaluate using accuracy, precision, recall, F1-score, and a confusion matrix.
6. Use Grad-CAM to visualize model attention.

## Dataset

- **OASIS Alzheimer's Detection (Kaggle)** -- brain MRI images organized into four classes: Non-Demented, Very Mild Dementia, Mild Dementia, Moderate Dementia. Based on the open-access OASIS aging and Alzheimer's imaging data.
- Kaggle: https://www.kaggle.com/datasets/ninadaithal/imagesoasis (downloaded in the notebook with `kagglehub`).
- OASIS background: https://www.oasis-brains.org

## Limitations and ethics

- The model is not a medical diagnostic system.
- Dataset labels may not match real clinical diagnosis perfectly.
- Splitting by image (not by patient) can cause leakage if scans from the same person land in both train and test.
- Real-world deployment would require clinical validation.
