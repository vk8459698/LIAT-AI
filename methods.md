# Methods Used: YOLO and Deep SORT for Object Detection and Tracking

This project implements real-time object detection and tracking using **Ultralytics YOLOv10** for detection and **Deep SORT** for multi-object tracking.

## YOLOv10 Detector

**File:** `yolo_detector.py`

The `YoloDetector` class uses the Ultralytics YOLOv10 model to perform object detection. It loads a pre-trained model (`best.pt`) and filters predictions by confidence.

### Key Methods
- `__init__(model_path, confidence)`  
  Loads YOLOv10 model and sets detection threshold.

- `detect(image)`  
  Runs inference and returns bounding boxes, class labels, and confidence scores.

- `make_detections(result)`  
  Converts raw YOLO output into a structured list of detections:
  - Format: `([x, y, w, h], class_id, confidence)`

## Deep SORT Tracker

**File:** `tracker.py`

The `Tracker` class wraps the Deep SORT algorithm, which uses appearance features and motion for ID-based tracking.

### Key Methods
- `__init__()`  
  Initializes the Deep SORT tracker with configurable parameters like `max_age`, `embedder`, etc.

- `track(detections, frame)`  
  Updates the tracker with new detections and returns:
  - `tracking_ids`: Persistent object IDs.
  - `boxes`: Bounding boxes in `[x1, y1, x2, y2]` format.

## Integration Pipeline

**File:** `yolo_detection_tracking.py`

- Initializes detector and tracker.
- Reads frames from a video.
- Applies YOLO detection and Deep SORT tracking.
- Draws bounding boxes and tracking IDs.
- Displays real-time FPS and visualization in OpenCV.

### Core Loop
```python
detections = detector.detect(frame)
tracking_ids, boxes = tracker.track(detections, frame)
