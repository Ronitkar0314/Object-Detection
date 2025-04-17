## 🚀 YOLOv5 Object Detection in Google Colab

This project demonstrates how to perform *object detection using YOLOv5* directly in Google Colab. It includes everything from cloning the repository to running inference on a custom image.

---

### 📸 What It Does

- 📦 Clones the [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5) repository
- ⚙ Installs all required dependencies
- 📥 Downloads pre-trained YOLOv5 models
- 🖼 Allows image upload for custom object detection
- 🧠 Runs YOLOv5 on the uploaded image and returns results with bounding boxes

---

### 📂 Features

- 🔧 Easy setup with just a few lines of code
- 🎯 Uses yolov5s.pt (small and fast pre-trained model)
- 📷 Upload your own image for detection
- 🧪 Real-time inference results visualized in Colab

---

### 🛠 How to Use

1. *Clone YOLOv5 and install dependencies*:
   python
   !git clone https://github.com/ultralytics/yolov5
   %cd yolov5
   !pip install -r requirements.txt
   

2. *Upload your image*:
   python
   from google.colab import files
   uploaded = files.upload()
   

3. *Run detection*:
   bash
   !python detect.py --weights yolov5s.pt --img 640 --conf 0.3 --source test.jpg
   

4. *Display output*:
   python
   from IPython.display import Image
   Image(filename='runs/detect/exp/test.jpg')
   

---

### 🧠 Note

- If the default model or custom weights like yolov5s-face.pt fail to download, ensure the URL is correct or manually upload the model.
- Detection may return no objects if the image doesn't contain recognizable classes from the COCO dataset.

---

### 🔍 Requirements

- Python 3.7+
- PyTorch
- Google Colab (for browser-based runtime)
- YOLOv5 dependencies (requirements.txt from the repo)

---

### 📌 Example Output

> A sample image is uploaded, and the detected objects (if any) are highlighted with confidence scores.

---# Object-Detection
