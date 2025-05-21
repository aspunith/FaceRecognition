# Face Recognition System

This repository contains the implementation of a Face Recognition System as part of the Deep Learning Specialization (Convolutional Neural Networks) by Andrew Ng. The project is inspired by concepts from FaceNet and DeepFace.

---

## 📑 Table of Contents
1. [Overview](#overview)
2. [Key Features](#key-features)
3. [Project Structure](#project-structure)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Workflow](#workflow)
7. [Technical Details](#technical-details)
8. [References](#references)
9. [License](#license)

---

## 🚀 Overview

The goal of this project is to build a face recognition system capable of:
- **Face Verification**: Verifying if a person is who they claim to be (1:1 matching).
- **Face Recognition**: Identifying a person among many (1:K matching).

The system uses a pre-trained model to encode face images into 128-dimensional vectors (embeddings). These embeddings are used for comparing and recognizing faces.

---

## ✅ Key Features

- **One-Shot Learning**: Can recognize new faces with just one image.
- **Pre-trained Model**: Leverages a powerful CNN trained on a large dataset.
- **Triplet Loss**: Optimized for learning robust facial features using triplet loss.
- **Dual Functionality**: Supports both verification and recognition scenarios.

---

## 📁 Project Structure

```plaintext
face-recognition/
├── Face_Recognition.ipynb     # Jupyter Notebook with full implementation
├── images/                    # Folder containing sample face images
├── utils.py                   # Helper functions for encoding and verification
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation
```

---

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/face-recognition.git
   cd face-recognition
   ```

2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   > **Note**: Compatible with Python 3.8+ and TensorFlow 2.x.

---

## 📌 Usage

1. Launch the Jupyter Notebook:
   ```bash
   jupyter notebook Face_Recognition.ipynb
   ```

2. Follow the notebook to:
   - Encode face images to embeddings.
   - Perform face verification (1:1) or recognition (1:K).
   - Add your own images to customize the face database.

---

## 🔄 Workflow

Here’s a high-level overview of the system's workflow:

1. **Input**: Face image(s).
2. **Preprocessing**: Resize to 160x160 and normalize.
3. **Encoding**: Use a CNN to convert faces into 128-D vectors.
4. **Comparison**: Compute distances between vectors.
5. **Output**: Verify or identify the person.

---

## 🧠 Technical Details

### 🔍 Face Verification vs. Face Recognition

| Task               | Description                          |
|--------------------|--------------------------------------|
| **Face Verification** | "Is this the claimed person?" (1:1) |
| **Face Recognition**  | "Who is this person?" (1:K)         |

### ✨ Triplet Loss Function

The model is trained using **Triplet Loss**, which ensures:
- The distance between **Anchor** and **Positive** (same person) is minimized.
- The distance between **Anchor** and **Negative** (different person) is maximized.

This helps the model learn a discriminative embedding space for faces.

---

## 📚 References

1. [FaceNet: A Unified Embedding for Face Recognition and Clustering](https://arxiv.org/pdf/1503.03832.pdf) - Florian Schroff, Dmitry Kalenichenko, James Philbin (2015).
2. [DeepFace: Closing the Gap to Human-Level Performance in Face Verification](https://research.fb.com/wp-content/uploads/2016/11/deepface-closing-the-gap-to-human-level-performance-in-face-verification.pdf) - Yaniv Taigman, Ming Yang, Marc'Aurelio Ranzato, Lior Wolf (2014).
3. [FaceNet GitHub Repository](https://github.com/davidsandberg/facenet).
4. Andrew Ng's Deep Learning Specialization - Coursera.

---

## 📄 License

This project is licensed under the MIT License. See the LICENSE file for details.

