# 🛰️ A User-Friendly Web Interface for Feature Extraction from Remote Sensing Satellite Images

---

## 🌍 Overview

This project enables pixel-wise land feature extraction from satellite imagery using an end-to-end deep learning pipeline. It empowers researchers, developers, and environmental planners with a **simple yet powerful web interface** to upload, analyze, and visualize segmented geographical data.

---

## 🔬 Key Features

- 🔍 **Semantic Segmentation with U-Net**  
  Pixel-level classification into land features: `Water`, `Vegetation`, `Road`, `Building`, `Land`, and `Background`.

- 🌐 **Web-Based Interface**  
  Upload satellite images directly via the frontend and receive color-coded segmentation masks in real time.

- 🧠 **Deep Learning Backend**  
  Python-based U-Net model trained on high-resolution Dubai Palm Beach images.

- ⚙️ **Microservice Architecture**  
  - Java Spring Boot – Handles API, user authentication, image upload
  - Python Flask/FastAPI – Runs the U-Net inference engine
  - JavaScript – Frontend interface and visualization

- 🌎 **Multi-region Testing**  
  - ✅ Trained on Dubai Palm Beach
  - 🧪 Tested on Jewar (India) and Hindon River regions for generalization

---

## 🧑‍💻 Tech Stack

| Layer          | Technology                              |
|----------------|------------------------------------------|
| Frontend       | ![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) ![JS](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) |
| Backend        | ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| Deep Learning  | ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white) ![U-Net](https://img.shields.io/badge/U--Net-SemanticSegmentation-blue?style=flat-square) |
| Deployment     | Localhost / Docker Ready                |

---

## 🗃️ Dataset

| Dataset        | Description                                                                  |
|----------------|-------------------------------------------------------------------------------|
| **Training**   | 70 High-res images from Dubai Palm Beach (with labeled masks of 6 classes)    |
| **Testing**    | 25 Images from Jewar region & 5 Images from Hindon River (Unseen during training) |

> ✅ Classes: `Water`, `Vegetation`, `Road`, `Building`, `Land`, `Unlabeled`

---

## 🖼️ Sample Segmentation Output

| Input Satellite Image | Segmented Output |
|------------------------|------------------|
| ![Input](https://via.placeholder.com/250x150?text=Satellite+Image) | ![Output](https://via.placeholder.com/250x150?text=Segmented+Mask) |

*Color Encodings:*  
🔵 Water | 🟢 Vegetation | ⚫ Road | 🟥 Building | 🟤 Land | ⬛ Background

---

## 🔧 System Pipeline

```mermaid
flowchart LR
    A[User Uploads Image] --> B[Spring Boot Backend]
    B --> C[Python U-Net Model API]
    C --> D[Image Preprocessing]
    D --> E[U-Net Inference]
    E --> F[Post-processing]
    F --> G[Return Segmentation Mask]
    G --> H[Frontend Visualization]

```


## ⚙️ Setup & Run

### 🔧 Prerequisites

- Python 3.8+
- Java 11+
- Node.js (Frontend, optional for expansion)
- Maven for Spring Boot
- TensorFlow, OpenCV, Flask/FastAPI

### 🛠️ Installation & Execution

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/feature-extraction-remote-sensing.git
   cd feature-extraction-remote-sensing

2. **Train or Load U-Net Model**
   ```bash
   python train_unet.py

3. **Start Python Inference Server**
   ```bash
   uvicorn app:app --reload

4. **Run Spring Boot Backend**
   ```bash
   cd spring-backend
   mvn spring-boot:run


## 👥 Contributors

| Name               | GitHub Username        |
|--------------------|-----------------------|
| Abhinay Goswami    | [Abhinay8506](https://github.com/Abhinay8506) |
| Divakar Sharma     | [Divakar-07](https://github.com/Divakar-07)  |
| Jay Kishor Thakur  | [jay-thakur-147](https://github.com/jay-thakur-147)  |





