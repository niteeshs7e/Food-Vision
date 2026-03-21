#  Food Vision – Image Classification with EfficientNet

##  Overview

Food Vision is a deep learning project that classifies food images into **101 categories** using **EfficientNet-B2** and **PyTorch**.

The project includes:

*  Transfer learning with EfficientNet
*  Gradio web interface
*  Hugging Face deployment
*  Reproducible runner notebook

---

##  Live Demo

👉 Try it here:
https://huggingface.co/spaces/nv45/food_vision_bigg

---

##  Features

* Upload any food image 
* Get **Top-5 predictions**
* See prediction confidence
* Fast inference using pretrained model

---

##  Model Details

* **Architecture:** EfficientNet-B2
* **Pretrained on:** ImageNet
* **Dataset:** Food101
* **Classes:** 101 food categories
* **Technique:** Transfer Learning

Classifier head:

```
Dropout(0.3)
Linear(1408 → 101)
```

---

## 📂 Project Structure

```
Food-Vision/
│
├── app.py                # Gradio app
├── model.py              # Model architecture
├── class_names.txt       # Class labels
├── food101_20_percent.pth
├── requirements.txt
├── examples/             # Sample images
│
├── notebooks/
│   └── runner.ipynb      # Reproducible notebook
│
├── README.md
└── LICENSE
```

---

## ⚡ Quick Start (Local Setup)

### 1️⃣ Clone the repo

```bash
git clone https://github.com/niteeshs7e/Food-Vision.git
cd Food-Vision
```

---

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

### 3️⃣ Run the app

```bash
python app.py
```

---

### 4️⃣ Open in browser

```
http://127.0.0.1:7860
```

---

##  Run in Google Colab

Click below to run instantly:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/niteeshs7e/Food-Vision/blob/main/notebooks/runner.ipynb)

---

##  Deploy on Hugging Face Spaces

You can deploy this project yourself in minutes.

### Step 1 — Create a Space

* Go to Hugging Face → Spaces
* Create a new Space
* Select **Gradio**

---

### Step 2 — Upload files

Upload these files from this repo:

```
app.py
model.py
class_names.txt
requirements.txt
examples/
food101_20_percent.pth (or auto-download)
```

---

### Step 3 — Push code

```bash
git clone https://huggingface.co/spaces/<username>/<space-name>
cd <space-name>

# copy files here

git add .
git commit -m "deploy food vision app"
git push
```

---

### Step 4 — Done 

Your app will be live automatically.

---

## 📦 Automatic Setup (Runner Notebook)

Instead of manual setup, you can run:

```
notebooks/runner.ipynb
```

This notebook will:

* Generate required `.py` files
* Download model & resources (zip)
* Prepare the full project

---

##  Future Improvements

* Train on full Food101 dataset
* Add nutrition/calorie estimation
* Improve UI/UX