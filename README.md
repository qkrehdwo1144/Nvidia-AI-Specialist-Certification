# Nvidia-AI-Specialist-Certification

## Dog Detection System for Pet Safety

---

### Background Information

Dogs have naturally become a part of our daily lives, being considered an integral part of our lives. However, as more people adopt dogs, concerns about the safety of their pets have also grown. This project aims to address these concerns by developing an AI-based system capable of detecting dogs in real time.

---

### Project Description

This project aims to develop an AI-based dog detection system capable of detecting dogs in real time. The system accurately detects the location of dogs, helping alleviate owners' concerns and enabling quick and flexible responses when a dog goes missing.

---

### Current Limitations

- **Various Appearances of Dogs:** Dogs vary greatly in size, appearance, and coat color depending on the breed, so a wide range of training data is necessary for accurate detection.
- **Obstructive Environment:** Since dogs move, they can be partially obstructed by furniture or objects in certain situations, which may affect detection performance.

---

### Training / Validation Video

- Training Video
  - ( )
- Validation Video
  - ( )

---

### Project Progress

#### **1. DarkLabel (labels)**
- **Go to the DarkLabel.exe file**
<p align="center">
  <img width="1263" alt="제목 없음" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/4a2dcb04dccdb0aa570a59edbac3f4dd92cf5a57/1.png">

- Click on "Open Video" to select the video for training.

<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/4a2dcb04dccdb0aa570a59edbac3f4dd92cf5a57/2.png">

<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/400b3bc642b1105cb94079a2f8f2ef30a17e0f7a/3..png"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/4a2dcb04dccdb0aa570a59edbac3f4dd92cf5a57/4.png">

- Ensure that it is set to "dog," then set it to "box + Label," uncheck "labeled frames only," and proceed with labeling
<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/400b3bc642b1105cb94079a2f8f2ef30a17e0f7a/5..png">

- After completing the labeling, click the "GT SAVE AS" button, select a folder, and save. You can then confirm that the labels are saved in a .txt file format.
<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/a78e1b6619fa402cc601ba53aefe888f05346cd2/6..png">

<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/a78e1b6619fa402cc601ba53aefe888f05346cd2/7.png">

- Check extracted labeling
<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/a78e1b6619fa402cc601ba53aefe888f05346cd2/8.png">

#### **3. Upload and prepare files before model training**
- Link your Google Drive to Colab + Clone and install the yolov5 repertoire

<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/9.png">

- Download Yolov5n model

<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/10.png">

- Upload files to yolov5 on google drive

<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/11.png">

#### **4. Model Learning**
---
<p align="center"><img src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/12.png">

<I set the epochs to 300, but the message "Stopping training early as no improvement observed in the last 100 epochs." appeared, and the training stopped.>

- **`train.py`**
    
  The training script for YOLOv5. It is used to train the model.
- **`-img 512`**
    
    Specifies the input image size.
    
    The training data is resized to 512x512 pixels before being fed into the model.
    
    Smaller sizes increase training speed but may reduce performance, while larger sizes require more computational resources.
- **`-batch 16`**
    
    Sets the batch size.
    
    It determines the number of images input into the model at one time.
    
    Larger batch sizes can speed up training but require more memory.
- **`-epochs 300`**
    
    Specifies the number of training iterations (epochs).
    
    The model will train on the entire dataset 300 times.
    
    A higher number of epochs increases training time but can improve model performance.
- **`-data /content/drive/MyDrive/yolov5/data.yml`**
    
    Path to the dataset configuration file.
    
    The `data.yml` file contains:
    
    - Dataset paths (train/val images and labels)
    - Number of classes
    - Class names
- **`-weights yolov5n.pt`**
    
    Specifies the pre-trained YOLOv5 model weights.
    
    `yolov5n.pt` refers to the Nano version of YOLOv5, which is lightweight and fast but may have relatively lower performance.
    
    Other options include: `yolov5s.pt`, `yolov5m.pt`, `yolov5l.pt`, `yolov5x.pt`.
- **`-cache`**
    
    Caches the dataset into memory to speed up training.
    
    When enabled, it reduces I/O time (file reading/writing) during training.

---

### Results

- **TensorBoard Visualization**
<p align="center">
    <img width="1021" alt="TensorBoard" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/13.png">
</p>

- **Confusion Matrix**
<p align="center">
    <img width="1021" alt="Confusion Matrix" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/14.png">
</p>

- **F1-Curve**
<p align="center">
    <img width="1021" alt="F1_curve" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/15.png">
</p>

- **labels_correlogram**
  <p align="center">
    <img width="1021" alt="labels_correlogram" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/16.jpg">
</p>

- **labels**
  <p align="center">
    <img width="1021" alt="labels" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/17.jpg">
</p>

- **P-Curve**
<p align="center">
     <img width="1021" alt="P-Curve" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/18.png">
</p>

- **PR-Curve**
<p align="center">
     <img width="1021" alt="P-Curve" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/19.png">
</p>

- **R-Curve**
<p align="center">
     <img width="1021" alt="P-Curve" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/20.png">
</p>

- **Result**
<p align="center">
     <img width="1021" alt="Result" src="https://github.com/qkrehdwo1144/Nvidia-AI-Specialist-Certification/blob/bf2e56e1e1907d527e3e51652d65b8dd80f06bbb/21.png">
</p>

- **Train batch**
