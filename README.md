# Finger Counter Project

This project detects hand gestures using a webcam and counts the number of raised fingers. The result is displayed with an overlay image corresponding to the detected finger count.

## Features

- **Real-time Hand Detection:** Uses Mediapipe for hand tracking and finger position detection.
- **Custom Overlay Images:** Displays an image corresponding to the number of raised fingers.
- **Dynamic Frame Rate Display:** Shows the frames per second (FPS) for real-time performance monitoring.

## Requirements

Ensure you have the following dependencies installed:

- Python 3.x
- OpenCV
- Mediapipe

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/jayambe36/finger-counter.git
   cd finger-counter
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv virenv
   source virenv/bin/activate  
   
   # On Windows:  virenv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Ensure the `FingerImages` folder is present with numbered images (e.g., `1.png`, `2.png`) for each possible finger count.

## Usage

1. Run the script:
   ```bash
   python finger_counter.py
   ```

2. Place your hand in front of the webcam. The program will detect raised fingers and display the corresponding overlay image.

## Code Overview

### Main Components

1. **Hand Detection Module:**
   - Located in `HandTracingModule.py`
   - Responsible for detecting hands and their positions.

2. **Overlay Images:**
   - Stored in the `FingerImages` folder.
   - Resized to `200x200` pixels for overlay on the video feed.

3. **Logic for Finger Counting:**
   - Checks the positions of finger tips and compares them with their respective base points.

### Key Variables

- `tipIds`: List containing indices of finger tips in Mediapipe's hand landmarks.
- `overlayList`: Stores the loaded and resized images for overlay.

## Folder Structure

```
.
├── FingerImages          # Contains overlay images
├── HandTracingModule.py  # Hand detection logic using Mediapipe
├── finger_counter.py     # Main script
├── requirements.txt      # Required dependencies
└── README.md             # Project documentation
```

## Examples

![Example Output](example_output.gif)

- Place your hand in front of the camera.
- The script will count the number of fingers and display the corresponding image.

## Known Issues

- Detection may fail in low-light conditions.
- Ensure the `FingerImages` folder contains correctly named files (`1.png`, `2.png`, etc.) to avoid indexing errors.

## Future Improvements

- Add support for both hands.
- Include additional gesture recognition features.
- Improve the UI for better user experience.

## Contributing

Contributions are welcome! If you encounter any issues or have suggestions, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

- [Mediapipe](https://google.github.io/mediapipe/) for providing robust hand-tracking models.
- [OpenCV](https://opencv.org/) for video capture and processing.

## Contact

For any inquiries, please contact:
- Email: smitrpatel19@gmail.com
- GitHub: [jayambe36](https://github.com/jayambe36)
