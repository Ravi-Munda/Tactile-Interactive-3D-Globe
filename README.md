# Tactile Interactive 3D Globe

**Explore the world through hand gestures.**

Tactile Interactive 3D Globe is a browser-based interactive globe that lets you explore a world visualization using hand movements detected by your device's camera. It combines geographic visualization with real-time hand tracking to create a more intuitive way to interact with a globe.

You can rotate the globe, control its zoom, and stop movement with simple gestures. Traditional controls are also available when you don't want to use the camera.

<p align="center">
  <a href="https://ravi-munda.github.io/Tactile-Interactive-3D-Globe/"><strong>Launch the Live Demo →</strong></a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Ravi-Munda/Tactile-Interactive-3D-Globe">View Source Code</a>
</p>

## Overview

Most interactive globe experiences rely on a mouse, trackpad, or touchscreen. This project explores an alternative: using hand gestures as an input method.

The application tracks hand landmarks using MediaPipe Hands and interprets movements to control the globe's rotation and zoom. A manual zoom slider and conventional pointer controls provide an alternative interaction method.

## Features

- **Gesture-based rotation** — move your open hand to rotate the globe.
- **Gesture-based zoom** — move your hand closer to or farther from the camera to adjust the zoom.
- **Stationary-hand detection** — holding your hand still pauses globe movement.
- **Fist gesture** — make a fist to stop the globe's movement.
- **Manual interaction** — rotate the globe with pointer controls and scrolling.
- **Zoom slider** — adjust the zoom level manually.
- **Visual hand tracking** — display detected hand landmarks and connections.
- **Live tracking status** — see whether tracking is active or the globe is stopped.
- **Browser-based experience** — access the application without installing a separate desktop application.

## Live Demo

**[Open Tactile Interactive 3D Globe](https://ravi-munda.github.io/Tactile-Interactive-3D-Globe/)**

For gesture controls, allow camera access when prompted. If camera access is unavailable, use the manual controls.

## How to Use

### 1. Open the application

Visit the live demo in a supported modern browser.

### 2. Enable hand tracking

Select **Enable hand tracking** and grant camera permission.

### 3. Control the globe

| Gesture or action | Result |
|---|---|
| Move an open hand horizontally | Rotate the globe horizontally |
| Move an open hand vertically | Adjust the globe's vertical rotation |
| Move your hand toward or away from the camera | Adjust zoom |
| Hold your hand still | Freeze globe movement |
| Make a fist | Stop globe movement |
| Drag with your pointer | Rotate manually |
| Scroll | Zoom manually |
| Use the zoom slider | Set zoom manually |

Gesture recognition depends on camera visibility, lighting, and how clearly your hand appears in the frame.

### 4. Stop hand tracking

Select **Stop hand tracking** when you want to turn off camera-based interaction.

## Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Interface styling and layout |
| JavaScript | Globe controls and gesture-processing logic |
| Plotly.js | Geographic globe visualization |
| MediaPipe Hands | Hand landmark detection and gesture input |
| MediaPipe Camera Utils | Camera-frame handling |
| MediaPipe Drawing Utils | Visualization of detected hand landmarks |

The application loads its JavaScript libraries from public CDNs, so an internet connection is required to load those dependencies.

## Run Locally

### Prerequisites

- A modern web browser.
- Python 3 for a simple local web server.
- An internet connection to load the external libraries.
- A camera if you want to use hand tracking.

### 1. Clone the repository

```bash
git clone https://github.com/Ravi-Munda/Tactile-Interactive-3D-Globe.git
cd Tactile-Interactive-3D-Globe
```

### 2. Start a local server

On Windows:

```bash
python -m http.server 8000
```

On macOS or Linux:

```bash
python3 -m http.server 8000
```

### 3. Open the application

Navigate to:

```text
http://localhost:8000
```

Using a local server is preferable to opening the HTML file directly, especially when testing camera access.

**Note:** Camera access generally requires a secure context, such as HTTPS or localhost, and permission from the user.

## How It Works

The application combines geographic rendering and hand tracking in a browser-based interface.

1. **Globe visualization:** Plotly.js renders the geographic visualization.
2. **Camera initialization:** MediaPipe Camera Utils supplies video frames to the hand-tracking pipeline after permission is granted.
3. **Hand landmark detection:** MediaPipe Hands detects landmarks on the visible hand.
4. **Gesture interpretation:** JavaScript analyses landmark positions and movement to identify supported gestures.
5. **Globe control:** The detected movements update the globe's rotation and zoom. A fist gesture stops movement, while a stationary hand freezes rotation.
6. **Manual fallback:** Pointer controls and a zoom slider allow interaction without hand tracking.

## Project Structure

```text
Tactile-Interactive-3D-Globe/
├── index.html   # Application, interface, styling, and JavaScript logic
├── README.md    # Project documentation
├── LICENSE      # GPL-3.0 license
└── SECURITY.md  # Security reporting information
```

## What I Learned

Building this project provided an opportunity to explore:

- Integrating third-party JavaScript libraries into a web application.
- Working with geographic data visualization.
- Using hand landmarks as an alternative input method.
- Mapping physical hand movements to on-screen interactions.
- Managing camera permissions and browser-based input.
- Building interactive interfaces with both gesture and manual controls.

## Future Improvements

Possible directions for future development include:

- More gesture options and customizable controls.
- Improved gesture stability and movement smoothing.
- Better mobile-device support and performance.
- Additional globe visualization settings.
- Accessibility improvements and clearer first-time instructions.
- More detailed documentation and demonstration screenshots.

## License

This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**. See the [LICENSE](LICENSE) file for details.

## Author

**Ravi Munda**

- GitHub: [@Ravi-Munda](https://github.com/Ravi-Munda)
- Repository: [Tactile-Interactive-3D-Globe](https://github.com/Ravi-Munda/Tactile-Interactive-3D-Globe)

---

*Exploring a more natural way to interact with the world.*
