# Multi-Angle Face Detection

An OpenCV notebook for detecting frontal and profile faces in video with Haar cascades, CLAHE preprocessing, and IoU-based duplicate removal.

## Highlights

- Frontal, left-profile, and right-profile detection
- Contrast enhancement for difficult lighting
- Non-maximum suppression for overlapping detections
- Labeled bounding boxes and live face counts
- Annotated video output

## Run

```bash
pip install jupyter opencv-python numpy
jupyter notebook Face_Detection.ipynb
```

Set the input video path in the notebook and run the cells in order. Press `Esc` to stop an interactive preview.

## Files

- `Face_Detection.ipynb` — complete detection pipeline
- `face_detection_output.mp4` — sample generated result

Haar cascades are lightweight but can produce false positives and missed detections. This project is a demonstration, not an identity or access-control system.
