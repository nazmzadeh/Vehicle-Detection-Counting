🚗 Vehicle Detection & Counting (YOLO26 + OpenCV)

This project performs real-time vehicle detection, tracking, and traffic counting using a YOLO-based model (YOLO26 compatible) and OpenCV.

It detects vehicles in video streams, tracks them across frames, and counts them when they cross a virtual line.

-- Features
Real-time vehicle detection using YOLO
Multi-object tracking with persistent IDs
Class filtering for vehicle-related classes
Traffic counting using virtual line crossing
Per-class vehicle counting (cars, buses, trucks, etc.)
Object trajectory visualization
Live overlay display

--Technologies Used
Python
Jupyter Notebook
OpenCV (cv2)
Ultralytics YOLO

--How It Works
Video input is read frame-by-frame
YOLO detects and tracks vehicles
Each vehicle gets a unique track_id
The center point of each vehicle is tracked
A horizontal counting line is defined
When a vehicle crosses the line:
It is counted once
The count is stored by vehicle type

--Output Visualization

The system displays:

Bounding boxes around vehicles
Unique tracking IDs
Center-point trajectories
A counting line
Real-time vehicle counts per class

🚀 Installation & Usage

1. Clone the repository
   git clone https://github.com/nazmzadeh/Vehicle-Detection-Counting.git
   cd Vehicle-Detection-Counting
2. Install dependencies
   pip install ultralytics opencv-python notebook

3. Run the project
   jupyter notebook

4. Open and run
   main.ipynb

## 🎥 Demo

![Vehicle Detection Demo](demo.gif)

👩‍💻Author
Nazakat Mammadzada
