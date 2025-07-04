# YOLO and Deep SORT based Object Detection and Tracking

This demo implements object detection and tracking using Ultralytics YOLOv10 and Deep SORT.

## Files

- `yolo_detection_tracking.py` – Main file that runs detection and tracking on a video feed
- `yolo_detector.py` – YOLOv10X detector wrapper
- `tracker.py` – Deep SORT-based tracker

## How to Run

1. Create a virtual environment:
   ```bash
   python -m venv venv
   ```

2. Activate the virtual environment:
   ```bash
   venv\Scripts\activate   # On Windows
   ```
   # or
   ```bash
   source venv/bin/activate   # On Linux/macOS
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Upload your YOLOv10 model to the `models/` folder
   or download a standard model (e.g. `yolov10x.pt`) from [Ultralytics](https://github.com/ultralytics/ultralytics),
   I have also added an Output.m4 for reference output.
   
5. Run the script:
   ```bash
   python yolo_detection_tracking.py
   ```
