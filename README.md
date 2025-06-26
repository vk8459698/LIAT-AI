Sure! Here's the updated **README.md** with everything in one concise block:

---

````markdown
# Yolo and Deep SORT based Object Detection and Tracking

This demo implements object detection and tracking using Ultralytics YOLOv10 and Deep SORT.

## Files
- `yolo_detection_tracking.py` – Main file that runs detection and tracking on a video feed
- `yolo_detector.py` – YOLOv10X detector wrapper
- `tracker.py` – Deep SORT-based tracker

## How to Run

1. Create a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate   # On Windows
   # or
   source venv/bin/activate   # On Linux/macOS
````

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Upload your YOLOv10 model to the `models/` folder
   or download a standard model (e.g. `yolov10x.pt`) from [Ultralytics](https://github.com/ultralytics/ultralytics)

4. Run the script:

   ```bash
   python yolo_detection_tracking.py
   ```

```

---

```
