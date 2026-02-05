# Classical OCR for CAPTCHA Images 

This repository contains the implementation of **Homework 2** for the **Computer Vision** course.  
The goal of this project is to build a complete **classical OCR pipeline** for CAPTCHA images **without using any machine learning or deep learning methods**.

---

## 🎯 Project Objective

The main objective is to recognize characters from CAPTCHA images using **traditional image processing techniques**, including:

- Image generation
- Noise addition and removal
- Deblurring and sharpening
- Image binarization
- Character segmentation
- Character recognition using similarity-based methods

---

## 🧠 Pipeline Overview

The overall processing pipeline is as follows:

Captcha Generation
↓
Noise & Blur Addition
↓
Preprocessing (Denoising, Deblurring, Binarization)
↓
Segmentation (Character Extraction)
↓
Resizing (64×64)
↓
Classical Character Recognition
↓
CSV Result Generation


---

## 🧩 Project Sections

### 🔹 Part 1: CAPTCHA Generation
- Generate random 3-character CAPTCHA images (letters and digits)
- Add Salt & Pepper noise
- Apply blur using image kernels
- Visual comparison between original and degraded images

### 🔹 Part 2: Preprocessing
- Noise removal using filtering techniques
- Deblurring or sharpening (e.g., Laplacian / Unsharp Mask)
- Image binarization using thresholding
- Removal of small connected components

### 🔹 Part 3: Segmentation
- Extract individual characters using connected components
- Report the number of extracted characters per image
- Resize characters to **64×64**
- Save segmented characters to disk

### 🔹 Part 4: Character Recognition
- Compare segmented characters with reference templates (Mapset)
- Use non-learning-based similarity measures such as:
  - Correlation
  - Mean Squared Error (MSE)
  - Structural similarity or histogram comparison
- Store predictions and similarity scores in a `.csv` file

---

## 🛠️ Requirements

- Python 3.x
- Jupyter Notebook
- Required libraries:
  ```bash
  numpy
  opencv-python
  matplotlib
  scipy
  pillow
  pandas
