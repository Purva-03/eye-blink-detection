
# Real-Time Eye Blink Detection and Counting System

## Project Overview

The Real-Time Eye Blink Detection and Counting System is a computer vision project developed using Python. It detects and counts human eye blinks in real time using a webcam.

The system uses facial landmark detection and Eye Aspect Ratio (EAR) calculations to identify when the eyes are open or closed.

## Features

- Real-time face detection using a webcam.
- Facial landmark detection using Dlib.
- Eye detection using 68 facial landmark points.
- Eye Aspect Ratio (EAR) calculation.
- Automatic eye blink detection and counting.
- Live display of blink count.
- CSV-based storage of blink count data.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| OpenCV | Image processing and webcam access |
| Dlib | Face detection and facial landmark detection |
| NumPy | Numerical computations |
| SciPy | Euclidean distance calculations |
| Pandas | Data handling and CSV storage |

## How It Works

1. **Webcam Initialization:** Captures live video using OpenCV.
2. **Face Detection:** Detects faces using Dlib's frontal face detector.
3. **Facial Landmark Detection:** Identifies 68 facial landmarks.
4. **Eye Region Extraction:** Identifies six landmark points around each eye.
5. **EAR Calculation:** Calculates the Eye Aspect Ratio using distances between eye landmarks.
6. **Blink Detection:** Detects a blink when EAR falls below a predefined threshold for consecutive frames.
7. **Blink Counting:** Updates and displays the total blink count.
8. **Data Storage:** Saves the blink count data in a CSV file.

## Eye Aspect Ratio (EAR)

The Eye Aspect Ratio is used to determine whether an eye is open or closed.

Formula:

EAR = (||p2-p6|| + ||p3-p5||) / (2 × ||p1-p4||)

Where:
- p1 to p6 represent six eye landmark points.
- Vertical distances help measure eye opening.
- Horizontal distance represents eye width.

A decrease in EAR indicates that the eye is closing.


## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Purva-03/eye-blink-detection.git
```

### 2. Navigate to the project directory

```bash
cd eye-blink-detection
```

### 3. Create a virtual environment

```bash
python -m venv .venv
```

### 4. Activate the virtual environment

For Windows:

```powershell
.venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Download the facial landmark model

Download the Dlib 68-point facial landmark predictor model and place the extracted `.dat` file inside the `models/` directory.

Ensure the model path in the Python script matches its actual location. Follow the model's applicable licensing terms.

### 7. Run the application

```bash
python src/blink_detection.py
```

Make sure your webcam is connected and accessible.

## Output

The application displays:
- Live webcam video.
- Detected face and eye landmarks.
- Real-time eye blink count.

The blink count is saved in a CSV file.

## Learning Outcomes

- Understanding real-time computer vision applications.
- Working with facial landmark detection.
- Image processing using OpenCV.
- Implementing Eye Aspect Ratio calculations.
- Developing Python-based computer vision applications.
- Handling and storing data using CSV files.

## Future Enhancements

- Calculate blink rate per minute.
- Add eye-closure duration monitoring.
- Develop a graphical dashboard for blink statistics.
- Add session-wise blink history.

## Author

**Purva Thakur**

- GitHub: https://github.com/Purva-03
- LinkedIn: https://www.linkedin.com/in/purva-thakur315/

---

**Project Category:** Computer Vision / Python Development
