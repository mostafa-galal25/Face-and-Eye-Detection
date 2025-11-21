# Real-Time Face and Eye Detection🚧

A simple and robust Python application utilizing OpenCV and Haar Cascade classifiers to detect faces and eyes in real-time video stream from a webcam.

# Key Features🚀

Real-Time Detection: Processes video input from the default webcam (index 0).

Face Localization: Draws a green rectangle around detected faces.

Nested Eye Detection: Detects eyes only within the localized face region for improved accuracy and efficiency, marking them with a blue rectangle.

Simple Interface: Displays the video feed in a window titled 'live stream'.

# Technologies Used🛠️

This project relies primarily on the powerful OpenCV library for computer vision tasks.

Language: Python

Library: OpenCV (cv2)

Algorithm: Haar Cascade Classifiers (specifically for frontal face and eyes).

# Prerequisites📦

Before running the project, ensure you have the following software installed:

Python (3.x recommended)

OpenCV library

The necessary Haar Cascade XML files.

# Installation and Setup💻

Follow these steps to set up the project locally:

Install OpenCV: If you don't have it installed, use pip:
pip install opencv-python

Obtain Haar Cascade Files: The project requires the following two XML files, which are standard in the OpenCV distribution:

haarcascade_frontalface_default.xml
haarcascade_eye.xml

Crucial Step:
In your current code, you are using absolute paths: 'C://Users//HP//Desktop//face_det//haarcascade_frontalface_default.xml'

You MUST place these two XML files inside the same directory as your Python script (.py file) and change the code to use relative paths for portability:
Before:

face_detect = cv2.CascadeClassifier('C://Users//HP//Desktop//face_det//haarcascade_frontalface_default.xml')
eye_detect = cv2.CascadeClassifier('C://Users//HP//Desktop//face_det//haarcascade_eye.xml')

After (Recommended):

face_detect = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')
eye_detect = cv2.CascadeClassifier('haarcascade_eye.xml')
(Make sure to upload the XML files to your GitHub repository along with the Python script.)

# How to Run▶️

Ensure your webcam is connected and accessible.

Run the Python script from your terminal:

python your_script_name.py
(Replace your_script_name.py with the actual name of your Python file.)

A window titled 'live stream' will open, showing the real-time detection.

To Exit: Press the 'x' key on your keyboard.

# Example Output🖼️.

(This is where you should ideally include a screenshot or GIF of the program running.)

# Contributing🤝.

Contributions are welcome!
If you have suggestions for improving accuracy, performance, or adding new features (like different Haar Cascade models), please feel free to:

Fork the repository.
Create a new feature branch (git checkout -b feature/AmazingFeature).
Commit your changes (git commit -m 'Add some AmazingFeature').
Push to the branch (git push origin feature/AmazingFeature).
Open a Pull Request.

# License📄.

Distributed under the MIT License. See LICENSE for more information.
