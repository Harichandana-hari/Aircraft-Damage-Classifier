# Aircraft Damage Detection and Captioning

This project classifies aircraft damage using a pre-trained **VGG16** model and generates descriptive captions using a **Transformer-based model (BLIP)**. It aims to automate aircraft damage inspection by detecting two types of damage — **dent** and **crack** — and providing human-readable descriptions for easier reporting.

---

## Project Overview

Aircraft damage detection is crucial for aviation safety and efficient maintenance. Manual inspection can be time-consuming and prone to error.  
This project provides:
- **Image Classification:** Classifies aircraft images into **dent** or **crack** categories using transfer learning with VGG16.
- **Image Captioning:** Generates descriptive captions and summaries for each image using BLIP (Bootstrapping Language-Image Pretraining).

---

## Project Goals

- Build an automated pipeline for detecting and classifying aircraft damage.
- Improve model generalization through data augmentation.
- Generate clear and concise image captions to assist maintenance teams.

---

## Dataset & Preprocessing

- **Dataset:** Aircraft images labeled as "dent" or "crack".
- **Preprocessing:** 
  - Used `ImageDataGenerator` from Keras for training, validation, and test sets.
  - Applied **real-time data augmentation** (rotation, zoom, flip) to improve generalization.
  - Kept validation and test sets unchanged for fair evaluation.

---

## Models Used

- **VGG16 (Feature Extraction):** Pretrained on ImageNet, fine-tuned for damage classification.
- **BLIP (Image Captioning):** Pretrained Transformer model used for generating captions and summaries.

---

## Tech Stack

- **Python**, **TensorFlow / Keras**
- **Hugging Face Transformers**
- **NumPy**, **Matplotlib**, **Pandas**

---

## Results

- **Classification Accuracy:** Achieved high accuracy in classifying dents and cracks.
- **Captions:** Model generates short, descriptive summaries like *"Aircraft wing with a visible dent near the edge."*

---

## Future Improvements

- Extend classification to multiple damage types (scratches, corrosion, etc.).
- Improve caption quality with domain-specific fine-tuning.
- Deploy as a web app for real-time inspection.
