# 🎯 Face Detection with OpenCV

A real-time face detection system built with Python and OpenCV that detects **frontal**, **left-profile**, and **right-profile** faces in video files using Haar Cascade classifiers with NMS-based duplicate removal.

---

## ✨ Features

- 🔍 **Multi-angle detection** — detects frontal, left-profile, and right-profile faces simultaneously
- 🔄 **Duplicate removal** — uses IoU-based Non-Maximum Suppression (NMS) to eliminate overlapping boxes
- 🌗 **CLAHE preprocessing** — improves detection accuracy in low-contrast or poorly-lit video frames
- 🏷️ **Labeled bounding boxes** — each detected face is labeled with its orientation (Front / Left / Right / Alt)
- 📊 **Live face counter** — shows total number of detected faces per frame in real time

---

## 🛠️ Requirements

- Python 3.8+
- OpenCV (`opencv-python`)
- NumPy

Install dependencies:

```bash
pip install opencv-python numpy
```

---

## 🚀 Usage

1. Place your video file in the project directory and rename it to `face_detection.mp4` (or update the path in the notebook).
2. Open the Jupyter Notebook:

```bash
jupyter notebook face_detection.ipynb
```

3. Run all cells. A window will open showing the video with face detection overlays.
4. Press **`ESC`** to stop playback.

---

## 🧠 How It Works

| Step | Description |
|------|-------------|
| **Frame capture** | Reads each frame from the input video |
| **Grayscale + CLAHE** | Converts to grayscale and applies contrast enhancement |
| **Multi-cascade detection** | Runs 3 Haar cascades (frontal, profile, alt) + horizontal flip for left profiles |
| **NMS filtering** | Removes duplicate/overlapping boxes using IoU threshold (0.4) |
| **Annotation** | Draws bounding boxes and labels on the original color frame |

---

## 📁 Project Structure

```
├── face_detection.ipynb   # Main notebook
├── face_detection.mp4     # Input video (not included)
└── README.md
```

---

## 📌 Notes

- The Haar cascade XML files are loaded automatically from OpenCV's built-in data directory — no manual download needed.
- For best results, use well-lit video with faces larger than 40×40 pixels.
- Detection speed depends on video resolution and your machine's CPU.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
