# 🎥 IP Camera Pro (Secure P2P)

![Version](https://img.shields.io/badge/version-3.0-blue.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg) ![WebRTC](https://img.shields.io/badge/tech-WebRTC%20%7C%20PeerJS-orange)

A powerful, **single-file** browser-based surveillance system. Turn any device (smartphone, tablet, laptop) into a security camera and view the feed remotely with full control.

**Now featuring a Host Approval System for enhanced security.**

## ✨ Key Features

* **🔒 Secure Connection:** New **Approval System**. The Host must explicitly approve incoming viewer connections.
* **📡 Peer-to-Peer:** Direct WebRTC connection. No video data passes through a central server.
* **🚨 Anti-Theft Mode:** Motion detection algorithm that auto-captures photos and logs incidents locally.
* **🗣️ Two-Way Audio:** "Walkie-Talkie" style push-to-talk communication from Viewer to Host.
* **🔦 Remote Hardware Control:** Toggle the Host's flashlight and control digital zoom remotely.
* **📂 Local Gallery:** View motion-detected security captures stored in the browser's IndexedDB.
* **⚡ Zero-Install:** Runs entirely in the browser. It is a single HTML file.
* **🌙 Cyberpunk UI:** Optimized for low-light environments and OLED screens.

## 🚀 Live Demo

[**Click here to Launch App**](https://wicam.netlify.app/)

## 📸 Screenshots

| Host Screen | Viewer Controls | Approval Modal |
|:---:|:---:|:---:|
| *(Add Screenshot)* | *(Add Screenshot)* | *(Add Screenshot)* |

## 🛠️ How to Use

### 1. Setting up the Host (Camera)
1. Open the app on the device you want to use as a camera.
2. Grant permissions for **Camera** and **Microphone**.
3. (Optional) Enable the **Anti-Theft** toggle to turn on motion detection.
4. Click **Start Host**.
5. A **4-Digit Code** will appear on the screen.

### 2. Connecting the Viewer (Remote)
1. Open the app on a second device.
2. Enter the **4-Digit Code** displayed on the Host device.
3. Click **Connect**.
4. **Wait:** The Host device will receive a popup requesting approval.

### 3. Approval Process (New!)
1. The Host device will show an **"Incoming Connection"** modal.
2. The Host clicks **APPROVE**.
3. The video stream begins immediately.

## 🔧 Technical Stack

* **Frontend:** Vanilla HTML5, CSS3, JavaScript (ES6+).
* **Networking:** [PeerJS](https://peerjs.com/) (WebRTC wrapper) for P2P data/media channels.
* **Storage:** IndexedDB for storing security logs/images locally.
* **Styling:** CSS Variables, Flexbox/Grid, Glassmorphism effects.

## 📦 Installation / Deployment

Since this is a single-file application, deployment is instant.

### Option A: GitHub Pages (Recommended)
1. Fork or upload this repository to GitHub.
2. Go to **Settings** -> **Pages**.
3. Select the `main` branch and click **Save**.
4. Your secure camera is now live at `https://<user>.github.io/<repo>`.

### Option B: Local Server
If running locally, you must use a local server (like Live Server in VS Code) or HTTPS, as browsers block camera access on `file://` protocols.

```bash
# If you have Python installed
python3 -m http.server 8000

# OR using Node.js http-server
npx http-server

