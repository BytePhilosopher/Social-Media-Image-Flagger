# 📛 Social Media Image Flagger using ML

A machine learning project that automatically flags inappropriate or harmful images from social media (like Facebook, Twitter, etc.) into multiple categories: NSFW, Violence, Hate/Abuse, and Normal. The goal is to support content moderation, prevent exposure to harmful visuals, and promote safer online spaces.

---

## 📌 Project Objective

To build a multi-class image classification system that can:
- Automatically detect and classify **harmful content** in images
- Flag images as:
  - `NSFW` (Not Safe For Work)
  - `Violence`
  - `Hate/Abuse`
  - `Normal` (Benign content)

This project simulates a real-world content moderation tool used by social media platforms or safety tech companies.

---

## 📂 Dataset Overview

We combine multiple publicly available datasets to cover each class:

| Class         | Dataset Source                                                       |
|---------------|-----------------------------------------------------------------------|
| **NSFW**      | [Yahoo Open NSFW](https://github.com/yahoo/open_nsfw) / Kaggle       |
| **Violence**  | [Violence Detection Dataset](https://github.com/brycedrennan/violence-detection-dataset) |
| **Hate/Abuse**| [Facebook Hateful Memes](https://ai.facebook.com/datasets/hateful-memes) |
| **Normal**    | [ImageNet](https://image-net.org/) / [Places365](http://places2.csail.mit.edu/) |

All images are resized, labeled, and stored in the `data/processed/` directory.

---

## 🧠 Model Architecture

- Pretrained CNN (e.g., **ResNet50**, **EfficientNet**) via transfer learning
- Final layer adapted for 4-class softmax output
- Loss: CrossEntropyLoss
- Optimizer: Adam
- Metrics: Accuracy, Precision, Recall, F1, Confusion Matrix

---

## 📁 Folder Structure

social_media_image_flagger/
│
├── data/
│ ├── raw/ # Original datasets
│ └── processed/ # Cleaned and labeled
│ ├── nsfw/
│ ├── violence/
│ ├── hate/
│ └── normal/
├── notebooks/ # EDA and model development
├── src/ # Core scripts (train, evaluate, dataloader)
├── models/ # Saved models (.pth)
├── outputs/ # Logs, metrics, confusion matrices
├── app/ # Streamlit app
├── config.yaml # Image size, batch size, class names
├── requirements.txt # Project dependencies
└── README.md # You're here!


---

## 🚀 How to Run

### 1. 📦 Install Dependencies
```bash
pip install -r requirements.txt



---
Developed by [Yostina Abera], inspired by real-world problems in content moderation and safety tech.

Datasets used are publicly available and credited to their original creators (Facebook AI, Yahoo, etc.).


---

Let me know if you'd like a version customized with your name, GitHub link, or Ethiopian context (e.g., mentions of conflict monitoring, education filters, etc.).
