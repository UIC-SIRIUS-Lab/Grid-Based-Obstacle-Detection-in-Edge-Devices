# 🧠 Grid-Based Obstacle Detection on Edge Devices

This repository contains the full implementation and dataset for the paper:

**“Lightweight Temporal Consistency for Grid-Based Obstacle Detection in Edge Devices”**  
_Omer Kurkutlu and Arman Roohi, University of Illinois Chicago_

📄 **[Paper PDF](https://sirius-lab.red.uic.edu/)**  

---

## 📌 Overview

We present a lightweight, platform-agnostic obstacle detection framework that converts grayscale images into a **6×8 binary obstacle matrix**, enabling real-time spatial reasoning on low-power devices. The pipeline supports:

- 🖥️ **YOLOv8n** on GPU-enabled desktops
- 🍓 **SSD-MobileNet v2 (TFLite)** on Raspberry Pi 2/3/4
- 🧠 **FOMO (Edge Impulse)** on microcontrollers like Arduino Nano 33 BLE

We also introduce a **temporal smoothing mechanism** that improves detection consistency without compromising latency.

➡️ **Watch the demo:**  
🎥 [Grid-Based Obstacle Detection with Temporal Smoothing (YOLOv8 Demo)](https://www.youtube.com/@omerkurkutlu6445/playlists)

> This video demonstrates our lightweight obstacle detection framework based on grid-based spatial abstraction and temporal smoothing.  
> The system uses a YOLOv8n model to detect obstacles and projects the bounding box outputs into a fixed 6×8 obstacle matrix. A smoothing mechanism is applied across frames to improve temporal consistency and reduce noise caused by occlusion, motion blur, or lighting variation.

⚙️ **Highlights:**
- YOLOv8n model inference on grayscale video  
- Grid-based binary occupancy map (6×8)  
- Temporal smoothing over recent obstacle matrices  
- Side-by-side comparison: raw vs. smoothed obstacle grids

---

## 🗂️ Repository Structure

📦 Grid-Based-Obstacle-Detection-in-Edge-Devices
├── yolov8/ # YOLOv8 training + dataset (YOLO format)
│ └── dataset_yolo/
│
├── tflite_ssd/ # TFLite SSD-MobileNet training
│ └── dataset_tflite/
│
├── fomo/ # Not included locally — hosted on Edge Impulse
│
├── projection/ # Grid conversion scripts
├── smoothing/ # Temporal smoothing implementation
├── evaluation/ # Evaluation + benchmarking tools
└── README.md

yaml
Copy
Edit

---

## 📊 Dataset Formats

We provide the same dataset in multiple formats, suitable for training and deploying across different platforms.

| Format     | Location               | Platform to Use | Download Dataset                                                          |
|------------|------------------------|-----------------|---------------------------------------------------------------------------|
| YOLOv8     | Hosted on OneDrive  | Desktop GPU     | [Edge Impulse Project](https://studio.edgeimpulse.com/public/your-project-id-here) |
| TFLite SSD | Hosted on OneDrive     | Raspberry Pi    | [Edge Impulse Project](https://studio.edgeimpulse.com/public/your-project-id-here) |
| FOMO       | Hosted on Edge Impulse | Microcontroller | [Edge Impulse Project](https://studio.edgeimpulse.com/public/your-project-id-here) |

The dataset includes **1,120 grayscale images** labeled with 11 obstacle-related classes:

barrel, cone, trunk, table, sign, box, pole, light, person, column, leaf



---


📜 Citation
Please cite our paper if you use this work:

bibtex
Copy
Edit
@article{kurkutlu2025gridobstacles,
  title     = {Lightweight Temporal Consistency for Grid-Based Obstacle Detection in Edge Devices},
  author    = {Omer Kurkutlu and Arman Roohi},
  journal   = {AI4AS 2025},
  year      = {2025},
  url       = {https://github.com/UIC-SIRIUS-Lab/Grid-Based-Obstacle-Detection-in-Edge-Devices}
}
💡 Acknowledgments
This work was supported in part by the National Science Foundation (NSF) under Grant Nos. 2504839 and 2448133.
Special thanks to the SIRIUS Lab at the University of Illinois Chicago.