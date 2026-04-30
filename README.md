# 🚗 Vehicle Detection, Tracking & Analysis (YOLO26 + OpenCV)

This project performs real-time vehicle detection, tracking, and traffic counting
using a YOLO-based model and OpenCV. It detects vehicles in video streams, tracks
them across frames, counts them when they cross a virtual line, and analyzes the
collected data to extract traffic insights.

## Features

- Real-time vehicle detection using YOLO
- Multi-object tracking with persistent IDs
- Class filtering for vehicle-related classes
- Traffic counting using virtual line crossing
- Per-class vehicle counting (cars, buses, trucks, etc.)
- Object trajectory visualization
- Live overlay display
- **Automated data pipeline — crossing events logged to structured CSV**
- **Exploratory data analysis with class distribution visualization**

## Technologies Used

Python, Jupyter Notebook, OpenCV (cv2), Ultralytics YOLO 2026, Pandas, Matplotlib, Seaborn

## How It Works

- Video input is read frame-by-frame
- YOLO detects and tracks vehicles
- Each vehicle gets a unique `track_id`
- The center point of each vehicle is tracked
- A horizontal counting line is defined
- When a vehicle crosses the line:
  - It is counted once
  - The count is stored by vehicle type
  - The event is logged to `traffic_log.csv` with timestamp, frame, track ID and class
- After the video ends, the log is analyzed and visualized in `analysis.ipynb`

## Output Visualization

The system displays:

- Bounding boxes around vehicles
- Unique tracking IDs
- Center-point trajectories
- A counting line
- Real-time vehicle counts per class
- Bar chart of vehicle class distribution

## **🚀 Installation & Usage**

1. Clone the repository

   ```python
    git clone https://github.com/nazmzadeh/Vehicle-Detection-Counting.git
    cd Vehicle-Detection-Counting
   ```

2. Install dependencies

   ```bash
   pip install ultralytics opencv-python notebook
   ```

3. Run the project

   ```bash
   jupyter notebook
   ```

4. Open and run

   ```bash
   main.ipynb
   ```

   This will process the video and generate `traffic_log.csv`

5. Open and run `analysis.ipynb`

   ```bash
   analysis.ipynb
   ```

   This will load the CSV and display the class distribution chart

## 🎥 Demo

![Vehicle Detection Demo](demo.gif)

👩‍💻Author
Nazakat Mammadzada
