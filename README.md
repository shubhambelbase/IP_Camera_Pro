# 🎥 IP Camera Pro (Secure P2P)

![Version](https://img.shields.io/badge/version-3.0-blue.svg) ![https://github.com/shubhambelbase/SelfhostIpwebcam/blob/main/LICENSE](https://img.shields.io/badge/license-MIT-green.svg) ![WebRTC](https://img.shields.io/badge/tech-WebRTC%20%7C%20PeerJS-orange)

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

| Host Screen | Approval | Viewer Screen |
|:---:|:---:|:---:|
| <img src="/host.jpg" width="250"> | src="/approval.jpg" width="250"> | | <img src="/viewer.jpg" width="250"> |


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

## 📦 Installation & How to Run

Because this app uses the Camera and Microphone, browsers require it to run in a **Secure Context (HTTPS)**. You cannot simply double-click the HTML file.

### Method 1: The Easiest Way (GitHub Pages) - RECOMMENDED
1.  Upload the `index.html` file to a GitHub repository.
2.  Go to **Settings** > **Pages**.
3.  Select `main` branch and click **Save**.
4.  Open the link provided (e.g., `https://username.github.io/repo`).
    * *Why this works:* GitHub provides free HTTPS certification automatically.

### Method 2: Vercel / Netlify (Drag & Drop)
1.  Go to [Netlify Drop](https://app.netlify.com/drop).
2.  Drag the folder containing your `index.html` onto the page.
3.  It will instantly generate a secure `https://...` link for you to use on your phone and PC.

### Method 3: Local Development (Advanced)
If you want to run it on your own computer:
1.  **Localhost:** You can run a local server (e.g., `python -m http.server`) and open `http://localhost:8000`. This will work **only on that computer**.
2.  **LAN Access:** If you want to access it from your phone on the same WiFi (e.g., `192.168.1.5:8000`), **it will fail** because it is not HTTPS. You would need to set up a self-signed certificate or use a tunneling service like **Ngrok**.

   ```bash
   # Example using Ngrok to expose local server via HTTPS
   npx http-server
   ngrok http 8080
   # Use the [https://....ngrok.io](https://....ngrok.io) link provided

