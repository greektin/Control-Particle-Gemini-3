# Aether Particles ✋✨

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Three.js](https://img.shields.io/badge/Three.js-r128-black)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Hands-orange)

**Aether Particles** is an interactive web experiment that combines WebGL rendering with Computer Vision. It generates a morphing 3D particle system (15,000+ points) that responds in real-time to your hand gestures via the webcam.

> **Note:** This project runs entirely in the browser using Vanilla JavaScript, Three.js, and Google MediaPipe. No backend is required.

## 🌟 Features

* **Real-time Hand Tracking:** Uses MediaPipe Hands to detect skeletal landmarks directly in the browser.
* **Gesture Control:**
    * **Rotate:** Move your hand around the screen to rotate the 3D model.
    * **Scale:** Pinch your thumb and index finger to scale the model size.
    * **Explode/Implode:** Move your hand closer to or further from the camera to scatter the particles or pull them tight.
* **Shape Morphing:** Seamlessly transition between mathematical 3D shapes:
    * 🌐 Sphere
    * ❤️ Heart
    * 🪐 Saturn (with rings)
    * 🌸 3D Flower/Rose Curve
* **Dynamic Visuals:** 15,000 individual particles with additive blending and dynamic coloring.
* **Glassmorphism UI:** A sleek, modern overlay built with Tailwind CSS.

## 🎮 How to Use

1.  Allow **Camera Access** when prompted.
2.  Wait for the status indicator to turn **Green** ("Tracking Active").
3.  Use your hand to control the particles:

| Gesture | Action |
| :--- | :--- |
| **Hand Position** | Controls the X/Y **Rotation** of the object. |
| **Pinch (Thumb + Index)** | Controls the **Scale/Zoom** of the particles. |
| **Distance (Hand Size)** | Controls the **Entropy/Spread**. Move hand away to explode, closer to condense. |

## 🚀 Getting Started

Because this project accesses the Webcam and loads ES modules via CDN, **it must be served via a local web server** (HTTPS or localhost). It will not work if you simply double-click the `.html` file (`file://` protocol) due to browser security restrictions.

### Option 1: VS Code (Recommended)
1.  Install the **Live Server** extension in VS Code.
2.  Open the folder containing `index.html`.
3.  Right-click `index.html` and select **"Open with Live Server"**.

### Option 2: Python
If you have Python installed, you can run a simple HTTP server in the terminal:

```bash
# Navigate to the project directory
cd path/to/project

# Python 3
python -m http.server 8000
