# Attendence-through-Face-recognition

The Face Attendance System is a Python script that leverages the face_recognition library along with OpenCV to create a simple yet effective attendance tracking system. This system captures live video feed from a camera, detects faces in real-time, and logs the attendance of recognized individuals into a CSV file.

## Table of Contents

- [Introduction](#introduction)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
  - [Getting Started](#getting-started)
  - [Customization](#customization)
- [Author](#author)
- [License](#license)

## Introduction

Managing attendance is a crucial aspect in various settings such as classrooms, meetings, and events. Traditional methods often involve manual recording or barcode scanning, which can be time-consuming and prone to errors. The Face Attendance System automates this process by utilizing facial recognition technology to accurately identify individuals and record their attendance.

## Dependencies

The following Python libraries are required to run the Face Attendance System:

- **face_recognition**: A simple library for facial recognition that wraps around dlib.
- **OpenCV (cv2)**: An open-source computer vision and machine learning software library.
- **numpy**: A fundamental package for scientific computing with Python.

## Installation

To install the required dependencies, you can use pip, the Python package manager. Run the following command in your terminal or command prompt:

```
pip install face_recognition opencv-python numpy
```

## Usage

### Getting Started

1. **Prepare Known Faces**: Ensure that you have images of each individual whose attendance you want to track. These images should be clear and include only the face of the individual. Save these images in a directory named `faces`.

2. **Update Known Faces**: Open the script `face_attendance.py` and update the `known_face_names` and `known_face_encodings` lists with the names and encodings of the known faces respectively. You can use the `face_recognition` library to generate face encodings for each known face.

3. **Run the Script**: Execute the script `face_attendance.py` using Python:
   ```
   python face_attendance.py
   ```

4. **Monitor Attendance**: The script will open a live video feed from the default camera. As recognized faces are detected, their attendance will be logged in a CSV file named with the current date (`YYYY-MM-DD.csv`) in the same directory as the script.

### Customization

- **Camera Configuration**: Adjust the camera index in the `cv2.VideoCapture()` function call if you're using a camera other than the default one (index 0).

- **Additional Functionality**: Modify the script to include additional functionality, such as saving images of unknown faces or integrating with a larger attendance tracking system.

## License

This project is licensed under the [MIT License](LICENSE).
