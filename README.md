# 🚀 TFG - Easy Low-Latency Video Streaming Setup

[![Download TFG](https://img.shields.io/badge/Download-TFG-brightgreen?style=for-the-badge)](https://github.com/ReiDasPaty/TFG/releases)

---

TFG is a tool designed to let you stream video with very little delay. It uses technologies like WebRTC, MediaMTX, and FFmpeg. You don’t need to be a tech expert to get it running on your Windows computer. This guide will take you step-by-step to download, install, and start streaming quickly.

## 📋 What is TFG?

TFG is a real-time video streaming system. It delivers video with very low delay. It uses common tools in the streaming world but wraps them into a setup ready to go using Docker. This means you can run the whole system with a few commands inside a controlled environment.

The system supports modern video streaming standards and is useful for events, security cameras, gaming streams, or any setup where you want live video with little lag.

---

## 💻 System Requirements

Before you start, please check the following requirements to ensure TFG will work on your PC:

- **Operating System:** Windows 10 or newer (64-bit)
- **Processor:** Intel i5 or equivalent AMD, 2.5 GHz or higher
- **Memory:** At least 8 GB RAM
- **Disk Space:** Minimum 5 GB free space for installation and streaming data
- **Network:** Stable internet connection (upload speed of at least 5 Mbps recommended)
- **Software Dependencies:** 
  - Docker Desktop for Windows (will guide you below)
  - Internet browser (Chrome, Firefox, Edge)

This setup will run Docker containers which package the streaming tools, so it's crucial that Docker runs smoothly on your computer.

---

## ⚙️ Setting Up Docker on Windows

TFG relies on Docker, which helps run all programs neatly inside containers. You need Docker installed before starting TFG.

### Steps to install Docker Desktop:

1. Visit the Docker Desktop Windows download page:  
   https://docs.docker.com/desktop/windows/install/

2. Download the installer by clicking the appropriate link for your Windows version.

3. Run the downloaded installer and follow the on-screen instructions.

4. After installation, open Docker Desktop and wait for it to finish starting. It will display a green light when ready.

5. Docker requires virtualization enabled in your BIOS. If you have issues during startup, check your PC’s BIOS settings for virtualization (Intel VT-x or AMD-V).

Once Docker is running, close Docker Desktop and proceed to the next step.

---

## 🎯 Download and Install TFG

You can download TFG from the official GitHub release page. This page contains all the files needed to run the streaming system, including ready-made container images.

### How to download:

1. Visit this page to download:  
   [Visit TFG Releases](https://github.com/ReiDasPaty/TFG/releases)

2. On the release page, look for the latest version. It is usually at the top.

3. Download the file named similar to `tfg-latest.zip` or a Docker-compose configuration file.

---

## ⚡ Running TFG on Windows

After you download and extract the files, follow these steps to get TFG running:

1. Open the folder with the extracted files.

2. Look for a file named `docker-compose.yml`. This file defines how the streaming system runs.

3. Open the Windows **Command Prompt**:
   - Press the **Windows key**, type `cmd`, and hit **Enter**.

4. In the Command Prompt, change directory to your extracted folder. For example:  
   ```
   cd C:\Users\YourName\Downloads\tfg-latest
   ```

5. Run the following command to start TFG:  
   ```
   docker-compose up
   ```

This command tells Docker to download necessary images and start the streaming services.

---

## 🔧 Using TFG

Once started, TFG will be running several services for video streaming:

- **WebRTC media server** ready to receive video at low latency
- **FFmpeg** for video processing
- **MediaMTX** for managing video streams
- **REST API** to control and monitor the system

### Accessing the system

- Open your web browser.
- Navigate to `http://localhost:8080` (or the port shown in the command line).
- You will find a simple interface to start streaming or connect sources.

### Streaming your video

- You can send video to TFG using compatible devices or streaming software that supports WebRTC or RTSP protocols.
- For example, use a webcam or an app like OBS Studio to send video to TFG.
- TFG converts and streams your video with very little delay.

---

## 🔄 Stopping TFG

To stop the streaming services:

1. Go back to the Command Prompt window where you ran `docker-compose up`.
2. Press **Ctrl+C** to stop the containers.
3. To completely remove the running containers, you can run:  
   ```
   docker-compose down
   ```

---

## 🛠 Troubleshooting

If you experience issues running TFG, try these steps:

- Make sure Docker Desktop is running and shows no errors.
- Check that virtualization is enabled on your PC.
- Restart Docker and your computer if needed.
- Verify that no other app is using port 8080 (or the port configured).
- Consult the logs by running:  
  ```
  docker-compose logs
  ```
- Make sure your firewall allows Docker and the streaming ports.

---

## 📥 Download TFG Now

Ready to get started? Visit the releases page and download the latest version of TFG. Follow the setup steps above to have your low-latency streaming system running on Windows.

[![Download TFG](https://img.shields.io/badge/Download-TFG-blue?style=for-the-badge)](https://github.com/ReiDasPaty/TFG/releases)

---

## 🧰 What’s Inside TFG?

- **WebRTC** for fast video communication.
- **MediaMTX** as a media server and stream manager.
- **FFmpeg** for high-quality video processing.
- **Docker Compose** to launch everything easily.
- **REST API** for control and configuration.

This integration ensures you can stream your video reliably and with minimal delay on a Windows machine without deep technical skills.