

## Green AI - Sapling Detection from Drone Imagery

### Project Overview

This project was developed as part of the **Green AI Hackathon at IIT Kharagpur's Kshitij**. The goal was to solve a **real-world reforestation problem in Odisha**, India.

We designed a computer vision pipeline to automatically detect and count:

* **Healthy saplings** (typically green),
* **Dead saplings** (typically brown or dry),
  from **drone-captured aerial images** of large grassland areas.

This system can support **environmental monitoring**, **reforestation efforts**, and **plantation success rate analysis** by automating sapling survival analysis.

---

### Problem Statement

Given drone images of large forest plantation areas in Odisha, identify:

* The number of **healthy saplings** (alive),
* The number of **dead saplings** (dried/brown),
* Their **locations** in the image.

---

###  Sample Image Input

* Format: JPEG (Captured via DJI drone)
* Resolution: High-definition
* Example file used: `DJI_20240608115621_0013_V.JPG`

---

###  Solution Approach

We used **color segmentation in the HSV color space** to differentiate saplings based on their color (green for healthy, brown for dead).
Contours are extracted to locate and count each sapling.

####  Techniques Used:

* Color thresholding in **HSV** space
* **Morphological operations** to remove noise
* **Contour detection** to locate individual saplings
* Bounding boxes to visualize detections

---

### 🧠 Key Results

* Detected saplings are marked with **green bounding boxes**
* Dead saplings are marked with **red bounding boxes**
* Printed count of healthy and dead saplings

---



### 📌 Future Enhancements

* Integrate object detection (YOLOv8 or Detectron2) for better accuracy
* Deploy on mobile drone software for real-time sapling health monitoring
* Use NDVI/NIR drone imagery to assess plant vitality
* Export bounding box coordinates for GIS-based plantation mapping

---

### 🤝 Acknowledgements

* Hackathon: **Kshitij Green AI**, IIT Kharagpur
* Region of focus: **Odisha, India**
* Image Source: **DJI drone (2024)**
