# SportSight: Real-Time Player & Ball Detection with YOLOv8

🎯 A computer vision system that processes football game footage to detect players and the ball, classify teams based on jersey colors, and generate an annotated video and CSV with tracking data.

![SportSight](https://img.shields.io/badge/YOLOv8-Ultralytics-blue) ![OpenCV](https://img.shields.io/badge/OpenCV-Tracking-green) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## 📌 Features

- ⚽ Detects players and ball using YOLOv8 object detection
- 🟥🟦 Assigns teams based on jersey color clustering (excluding green field)
- 📦 Saves structured tracking results to a CSV
- 🎥 Generates an annotated video with labeled bounding boxes
- 🔁 Processes video frame-by-frame (with optional frame skipping)

---

## 🧠 Technologies Used

- [YOLOv8](https://docs.ultralytics.com) by Ultralytics
- [OpenCV](https://opencv.org/) for image processing and video output
- [NumPy & Pandas](https://pandas.pydata.org/) for data handling
- Optional: [EasyOCR](https://github.com/JaidedAI/EasyOCR) for jersey number recognition (currently commented)

---

## 🚀 How It Works

1. Load input football match video.
2. Use YOLOv8 to detect people (players) and sports balls.
3. Mask out green areas (field) and extract dominant jersey color per player.
4. Use k-means clustering to assign team 0 or 1 based on jersey color.
5. Draw bounding boxes on the frame with team-based color (red/blue) and save video.
6. Export tracking data to CSV with object type, frame number, bounding box, and team.

---

