#  AR Gesture Interaction Interface

###  System Demonstration(demo video)
https://github.com/Devzz2302/AR_Gesture_System/blob/main/demo.mp4?raw=true

> **Status:** Operational | **Tech:** Mediapipe + JavaScript

---

##  Project Overview
This is a high-fidelity AR interaction prototype designed for touchless environments. Using Computer Vision, the system maps human hand gestures to digital triggers in real-time, allowing users to interact with virtual elements via their laptop camera.

---

##  Live Demo
**[👉 Click Here to Open the AR Interface](https://devzz2302.github.io/AR_Gesture_System/)**

---

##  Supported Gestures & Actions
The interface recognizes specific skeletal configurations to execute commands:

| Gesture | Visual Trigger | System Action |
| :--- | :--- | :--- |
| **Victory (✌️)** | Holographic Badge | Overlays a "Verified" encrypted status on screen. |
| **Thumbs Up (👍)** | System Flash | Triggers a full-screen "photon flash" for data capture. |
| **No Hand** | UI Reset | Reverts system to "Scanning" mode automatically. |

---

##  Technical Implementation
* **Landmark Tracking:** Utilizes the Mediapipe Hand model to track 21 distinct 3D points.
* **Gesture Logic:** The system uses coordinate-based triggers. For example, the "Victory" sign is detected when:
    * $Index\_Tip.y < Index\_Knuckle.y$
    * $Middle\_Tip.y < Middle\_Knuckle.y$
    * $Ring\_Tip.y > Index\_Knuckle.y$
* **Frontend:** Custom CSS "Glassmorphism" UI with real-time scanline animations for a professional dashboard feel.

---

##  Reflection & UX Strategy
The core of this "Human Interaction" task was creating a seamless loop between user movement and system response. I focused on:
1. **Visual Scaffolding:** Drawing the skeleton so users know they are being tracked.
2. **Intentional Triggers:** Using a state-lock for the "Thumbs Up" flash to ensure the interaction feels crisp and not accidental.
3. **Accessibility:** Using high-contrast glows (Purple/Orange) to signal successful triggers to the user.
