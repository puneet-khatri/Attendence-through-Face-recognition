# Attendence-through-Face-recognition

This Python script utilizes the face_recognition library to create a simple face attendance system. It captures video from the default camera (or any specified camera) and detects faces in real-time. When a recognized face is detected, it logs the attendance of the person by recording their name and the current time into a CSV file.

## Dependencies

- face_recognition
- OpenCV (cv2)
- numpy

## Installation

Make sure you have Python installed on your system. Then, install the required dependencies using pip:

```
pip install face_recognition opencv-python numpy
```

## Usage

1. Ensure that you have a known image of each individual whose attendance you want to track. 
2. Save these images in the `faces` directory.
3. Update the `known_face_names` and `known_face_encodings` lists with the names and encodings of the known faces respectively.
4. Run the script by executing `python face_attendance.py`.
5. The script will open a live video feed. As recognized faces are detected, their attendance will be logged in a CSV file named with the current date (`YYYY-MM-DD.csv`).

### Note:

- Ensure that the camera is correctly connected and accessible.
- Adjust the camera index in the `cv2.VideoCapture()` function call if you're using a camera other than the default one (0).

## Customization

- You can modify the script to include additional functionality, such as saving images of unknown faces or integrating with a larger attendance tracking system. Also you can suggest me to add some features.

## License

This project is licensed under the [MIT License](LICENSE).
