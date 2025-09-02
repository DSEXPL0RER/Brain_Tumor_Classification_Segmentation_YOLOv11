# Brain Tumor Classification and Area Segmentation Using YOLOv11 Framework

This project implements a **deep learning–based system for brain tumor detection and segmentation** using the **yolo11s-seg.pt model**. The system automatically identifies the tumor type and regions in brain MRI images, generates segmentation masks, and estimates tumor size relative to the brain area.

## 🌐 Live Demo  
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://braintumor-classificationsegmentationyolov11-tqzk6g5wzsbptq3cuh.streamlit.app)

The project includes:

* A **Streamlit web application** (`app.py`) for real-time tumor detection and mask visualization.
* Kaggle Notebooks for **model training, testing, and inference**.
* Support for **downloading detection results, tumor masks, and size estimation overlays**.

---

## 🚀 Features

* Upload brain MRI images (`.jpg`, `.jpeg`, `.png`).
* Detect brain tumors with YOLO11s-seg.
* Generate tumor segmentation masks.
* Calculate tumor size as a percentage of brain area.
* Option to download:

  * Tumor detection results
  * Segmentation masks
  * Tumor size estimation overlays
  * Adjustable confidence threshold and display settings.

---

## 📂 Project Structure

```
├── app.py                          # Streamlit web application
├── requirements.txt                # Dependencies for deployment
├── YOLOv11s_Model_Training.ipynb   # Notebook for training the model
├── Model_Prediction_Demo.ipynb     # Notebook for model evaluation
├── best.pt                         # Trained yolo11s-seg.pt model weights
└── README.md                       # Project documentation
```

---

## ⚙️ Installation & Setup

1. **Clone the repository**

```bash
git clone https://github.com/DSEXPL0RER/Brain_Tumor_Classification_Segmentation_YOLOv11.git
cd brain-tumor-detection
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Run the Streamlit app**

```bash
streamlit run app.py
```

---

## 🧾 Requirements

Dependencies are listed in `requirements.txt`:

```
streamlit
opencv-python-headless
numpy
pillow
ultralytics
```

---

## 📊 Dataset

The dataset used in this project is based on **BRATS (Brain Tumor Segmentation Challenge) MRI scans**, which were **collected from Hayatabad Medical Complex (HMC) Hospital, Peshawar**.
It includes multiple tumor categories such as **Glioma, Meningioma, and Pituitary tumors**.

---

## 📊 Model

The project uses the **yolo11s-seg.pt model** (small segmentation variant of YOLO11) from [Ultralytics](https://docs.ultralytics.com).

* Task: **Instance Segmentation**
* Model name: `yolo11s-seg.pt`
* Trained on: Brain MRI dataset (Glioma, Meningioma, Pituitary).
* Training and experiments were conducted on **Kaggle GPU** for faster performance.

---

## 🔄 How It Works

1. **Upload MRI Image** → User uploads a brain MRI image in the web app.
2. **Model Prediction** → The YOLO11s-seg model detects tumor regions.
3. **Segmentation Mask** → The tumor area is segmented at the pixel level.
4. **Area Estimation** → Tumor size is calculated as a percentage of the brain area.
5. **Results & Downloads** → Users can view and download detection images, masks, and area estimation overlays.

---

## 🎯 Use Cases

* Medical research and academic purposes.
* Assisting radiologists in tumor localization.
* Demonstrating deep learning applications in healthcare.

---

## ⚠️ Disclaimer

This project is **for educational and research purposes only**. It is **not intended for clinical diagnosis or medical use**.

---

## 🙌 Acknowledgements

* [Ultralytics YOLO](https://github.com/ultralytics/ultralytics)
* **BRATS Dataset (HMC Hospital MRI scans)**
* Kaggle (GPU support for training and testing)
* Open source medical imaging resources

---

✨ Built with Python, Streamlit, OpenCV, and yolo11s-seg.
