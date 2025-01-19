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

#### **3. Training Data with YOLOv5 in Colab**
- Link your Google Drive to Colab
  
