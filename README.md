# Drowsiness Detection System

This project implements a Drowsiness Detection System using Python, OpenCV, and dlib. The system monitors a user's eye aspect ratio (EAR) through a webcam feed to detect signs of drowsiness, alerting the user with an alarm sound when drowsiness is detected.

## Features

- **Real-time Eye Aspect Ratio Calculation**: Uses facial landmarks to calculate the EAR for both eyes.
- **Drowsiness Alert**: Plays an alarm sound when the user's EAR falls below a specified threshold for a set number of frames, indicating potential drowsiness.
- **Visual Feedback**: Draws the eye contours on the video feed for better visualization.

## Requirements

- Python 3.x
- OpenCV
- dlib
- imutils
- pygame

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd drowsiness-detection
   ```

2. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Download the pre-trained facial landmark predictor:

   - Place the `shape_predictor_68_face_landmarks.dat` file inside the `models` folder.

4. Place an audio file named `music.wav` in the root directory of the project, which will be used as the alert sound.

## Usage

Run the following command to start the drowsiness detection system:

```bash
python drowsiness_detection.py
```

- The system will start capturing the video feed from your webcam.
- If drowsiness is detected, an alert message will appear on the screen, and an alarm sound will play.
- Press `q` to exit the program.

## Configuration

- **Threshold (`thresh`)**: Adjust the EAR threshold value in the code to change the sensitivity of drowsiness detection.
- **Frame Check (`frame_check`)**: Change the number of consecutive frames required to trigger the alert.

## How It Works

1. The program captures video from the webcam.
2. It detects faces in the frame and identifies eye regions using facial landmarks.
3. The EAR is calculated for both eyes; if the EAR falls below the threshold for a specified number of frames, an alert is triggered.

## Troubleshooting

- Ensure that the `shape_predictor_68_face_landmarks.dat` file is correctly placed in the `models` folder.
- Make sure the webcam is functioning properly.
- Check that the required packages are installed.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
