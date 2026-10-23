# ✋ Hand Gesture Detection

**A real-time hand gesture detection web application powered by MediaPipe Hands, HTML, CSS, and JavaScript.**

Recognize hand gestures through your webcam, visualize hand landmarks, view detection history, and hear gesture feedback—all within a web browser.

<p align="center">
  <a href="https://github.com/gaurav7sni/hand-gesture-detection">
    <img src="https://img.shields.io/badge/Project-Hand%20Gesture%20Detection-blue" alt="Project">
  </a>
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-yellow" alt="JavaScript">
  <img src="https://img.shields.io/badge/MediaPipe-Hands-brightgreen" alt="MediaPipe Hands">
  <img src="https://img.shields.io/badge/Platform-Web-orange" alt="Web Application">
</p>

---

## 📌 Overview

**Hand Gesture Detection** is a browser-based computer vision project that uses a webcam to detect hand landmarks and interpret hand poses as recognizable gestures.

The application combines MediaPipe Hands for hand tracking with a JavaScript-based gesture classification engine. It processes the detected hand landmarks, evaluates finger positions, and displays the recognized gesture in the interface.

The project explores how computer vision can make web applications more interactive without requiring a separate desktop application or a Python-based backend.

## ✨ Features

- **Real-time hand tracking:** Detect and track hands using a webcam.
- **Two-hand support:** Configured to track up to two hands.
- **Gesture recognition:** Identify supported hand poses using a JavaScript gesture classification engine.
- **Landmark visualization:** Display hand landmarks and their connections on a canvas.
- **Detection history:** View a timestamped log of recognized gestures.
- **Text-to-speech feedback:** Hear recognized gesture labels using the browser's speech synthesis API.
- **Gesture stability controls:** Adjust the hold threshold to help reduce rapidly changing predictions.
- **Speech rate control:** Adjust the speed of spoken feedback.
- **Display controls:** Toggle the hand skeleton and adjust the camera orientation.
- **Camera error handling:** Display feedback when camera access is unavailable or denied.
- **Browser-based interface:** No separate desktop application is required.

## 🎥 Demo

**Live Demo:** [Add your deployed application URL here]

**Screenshots:**

<!-- Add a screenshot after uploading it to the repository. -->
<!-- Example: ![Hand Gesture Detection Demo](screenshots/demo.png) -->

*Screenshot coming soon.*

A short screen recording or GIF demonstrating live detection would also be useful here.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Styling and responsive interface |
| JavaScript | Gesture classification and application logic |
| MediaPipe Hands | Hand landmark detection and tracking |
| MediaPipe Camera Utils | Camera frame handling |
| Canvas API | Drawing hand landmarks and connections |
| WebRTC / MediaDevices API | Webcam access through `getUserMedia()` |
| Web Speech API | Text-to-speech feedback |
| jsDelivr CDN | Loading MediaPipe libraries |

The application currently uses a single HTML file containing its interface, styling, and JavaScript logic.

## 📂 Project Structure

```text
hand-gesture-detection/
├── README.md
├── hand-detection.html
├── screenshots/
│   └── demo.png
└── LICENSE
```

**Notes:**
- `hand-detection.html` is the suggested filename for the application. If your uploaded file has a different name, use that filename in the instructions below or rename the file.
- `screenshots/demo.png` is optional and should be added when you have a real application screenshot.
- Add a `LICENSE` file only after choosing the license under which you want to distribute the project.

## 🚀 Getting Started

### Prerequisites

You will need:

- A modern web browser.
- A working webcam.
- An internet connection to load the MediaPipe libraries from the CDN.
- Permission to access the camera.

### 1. Clone the Repository

Open your terminal and run:

```bash
git clone https://github.com/gaurav7sni/hand-gesture-detection.git
cd hand-gesture-detection
```

### 2. Start a Local Web Server

For the simplest setup, use Python's built-in HTTP server. You do not need to install additional Python packages for this step.

```bash
python3 -m http.server 8000
```

### 3. Open the Application

Visit:

```text
http://localhost:8000/hand-detection.html
```

If your HTML file has a different name, replace `hand-detection.html` with the actual filename.

### 4. Allow Camera Access

When prompted by your browser, allow camera access. Position your hand within the camera frame and try one of the supported gestures.

> **Important:** Camera access generally requires a secure context, such as `localhost` or an HTTPS-hosted website. Opening the HTML file directly may not work in every browser configuration.

## 🖐️ How to Use

1. Open the application in your browser.
2. Allow access to your webcam.
3. Position your hand clearly within the camera frame.
4. Try different supported hand gestures.
5. Observe the recognized gesture and the hand landmark visualization.
6. Review the detection history to see previously recognized gestures.
7. Enable or disable the hand skeleton as needed.
8. Adjust the gesture hold threshold and speech rate to suit your preference.

**Tip:** Good lighting, a clearly visible hand, and keeping your hand within the camera frame can help improve tracking.

## ⚙️ How It Works

The application follows this general workflow:

1. **Camera input:** The browser obtains a live video stream using the MediaDevices API.
2. **Hand tracking:** MediaPipe Hands processes the video frames and estimates hand landmarks.
3. **Feature evaluation:** The JavaScript gesture engine evaluates landmark positions and finger configurations.
4. **Gesture classification:** The application compares the detected hand configuration with the gesture logic implemented in the code.
5. **Stability handling:** A hold threshold helps prevent the interface from reacting immediately to every temporary change in the predicted gesture.
6. **Visual feedback:** The application draws the hand landmarks and displays the recognized gesture.
7. **Additional feedback:** Recognized gestures can be recorded in the detection history and spoken aloud through the browser's speech synthesis functionality.

### Detection Configuration

The current MediaPipe Hands configuration includes:

| Parameter | Value |
|---|---|
| Maximum number of hands | 2 |
| Model complexity | 1 |
| Minimum detection confidence | 0.65 |
| Minimum tracking confidence | 0.55 |

These are configuration values, not measured accuracy results.

## ⚠️ Limitations

- **Recognition is not perfect:** Results can vary with lighting, camera quality, hand position, and gesture execution.
- **Supported gestures are implementation-dependent:** The application can only recognize gestures covered by its current classification logic.
- **Not a complete sign language translator:** Recognizing individual hand poses is not equivalent to interpreting sign language, which may require movement, context, facial expressions, and grammar.
- **No published accuracy benchmark:** Formal testing has not yet established a measured accuracy percentage.
- **Browser compatibility needs testing:** Camera access, speech synthesis, and MediaPipe loading may behave differently across browsers and devices.
- **Internet connection required:** The current implementation loads MediaPipe scripts from an external CDN.
- **Camera permission required:** The application cannot process a live webcam stream without access to the camera.

## 🗺️ Roadmap

Potential future improvements:

- [ ] Add screenshots and a live online demo.
- [ ] Test and document compatibility across major browsers.
- [ ] Benchmark gesture recognition under different lighting conditions.
- [ ] Improve gesture classification and prediction stability.
- [ ] Add configurable options for supported gestures.
- [ ] Improve mobile and small-screen usability.
- [ ] Add a more detailed detection statistics panel.
- [ ] Explore additional gesture-based interactions.

Suggestions and contributions are welcome.

## 🤝 Contributing

Contributions, suggestions, and bug reports are welcome.

1. Fork this repository.
2. Create a branch for your changes:

   ```bash
   git checkout -b feature/your-feature
   ```

3. Make and test your changes.
4. Commit your work:

   ```bash
   git commit -m "Add your feature"
   ```

5. Push the branch and open a pull request.

Please describe the changes you made and include screenshots or reproduction steps when reporting interface issues.

## 📄 License

A license has not been specified in this README.

Before distributing the project, choose a license and add the corresponding `LICENSE` file to the repository. If you choose the MIT License, include the complete MIT license text and confirm that it is appropriate for the code and assets you distribute.

## 🙌 Acknowledgments

- **[MediaPipe](https://mediapipe.dev/)** for the hand landmark detection and tracking technology.
- **[jsDelivr](https://www.jsdelivr.com/)** for CDN delivery of the MediaPipe libraries.
- The browser's built-in camera, Canvas, and speech synthesis APIs for interactive functionality.

## 📬 Contact

**Developer:** Gaurav Jha

- **GitHub:** [@gaurav7sni](https://github.com/gaurav7sni)
- **Repository:** [hand-gesture-detection](https://github.com/gaurav7sni/hand-gesture-detection)
- **LinkedIn:** [Add your LinkedIn profile link here]

If you find a bug or have an idea for an improvement, feel free to open an issue in the repository.

---

⭐ If you find this project interesting, consider starring the repository!
