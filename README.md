# AI_CODE-PROFESSIONAL-
👁️ AI Vision & Safety Professional Suite
Welcome! This repository houses a collection of professional-grade Computer Vision and AI solutions designed for industrial safety, monitoring, and advanced analytics.

My goal with this code is to turn raw video data into actionable insights—helping workplaces stay safe and efficient using state-of-the-art object detection and tracking technologies.

🚀 What's Inside?
This toolkit is divided into three main pillars of industrial AI application:

1. 🦺 Smart PPE Compliance Detection
Automated safety monitoring to ensure personnel are properly protected in hazardous zones.

Zone-Based Monitoring: Defines specific safety zones (e.g., Left vs. Right areas) with unique safety requirements. For example, a "High Hazard" zone might require a PVC suit and goggles, while a "Walkway" only requires a helmet.

Individual Tracking: Uses DeepSort to track individual workers (assigning unique IDs), ensuring that safety violations are logged per person over time, rather than just counting frame-by-frame errors.

Dynamic Requirements: Easily configurable to check for helmets, vests, safety shoes, goggles, and more.

Violation Logging: Automatically generates timestamped logs of every safety breach for auditing.

Files: zone_based_class_detection.py, user_based_detection.py, log_detect.py

2. 🚜 Intelligent Vehicle Analytics (Forklift Speed & Load)
Physics-aware tracking system for industrial vehicles.

Speed Estimation: Uses Kalman Filters to smooth tracking data and calculate the real-world speed of forklifts in km/h.

Load Detection: Intelligently estimates if a forklift is carrying a load based on visual heuristics (bounding box dynamics).

Smart Safety Limits: Applies different speed limits dynamically! It knows that a loaded forklift should drive slower than an empty one and alerts operators accordingly.

Data Export: exports a detailed CSV report containing max speeds, average speeds, and total distance covered for every vehicle tracked.

File: speed_detection_.py

3. 🎨 Crystal-Clear Visualizations
Because data is only useful if you can read it.

Smart Labeling: A set of algorithms designed to solve the "cluttered screen" problem in computer vision.

Techniques Included:

Smart Positioning: Finds empty spaces on the screen to place text so it never covers the object.

Hierarchical Stacking: Organizes labels cleanly when multiple objects overlap.

Side-Panel View: Moves detailed data to a dedicated sidebar to keep the video feed pristine.

File: desiredLabelling.ipynb

🛠️ Tech Stack
This project is built on robust, industry-standard open-source libraries:

Object Detection: Ultralytics YOLO (v8/v11) for high-speed, accurate recognition.

Tracking: deep-sort-realtime for associating objects across frames.

Computer Vision: OpenCV for image processing and drawing visuals.

Math & Physics: NumPy and SciPy for vector calculations and assignment problems.

💻 Getting Started
Clone the Repo

Bash: git clone https://github.com/manojdey224/AI_CODE-PROFESSIONAL-.git
cd AI_CODE-PROFESSIONAL-
Install Dependencies The projects rely on similar core libraries. You can install them via pip:

Bash: pip install ultralytics opencv-python numpy deep-sort-realtime supervision
Run a Module

For PPE Detection:

Bash: python "zone_based_class_detection (1).py" --video path/to/your/video.mp4 --classes_left helmet --classes_right safety_vest
For Speed Detection: (Update the VIDEO_PATH variable inside the script first)

Bash: python speed_detection_.py
📝 License
This project is intended for professional and educational use. Please feel free to explore, fork, and improve upon the code!
