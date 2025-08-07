# OpenCV Streaming 📹

This project demonstrates real-time video streaming between a client and a server using OpenCV and Python. The client captures video from a webcam, compresses it, and sends it to the server over a UDP socket. The server receives the video stream, decodes it, and displays it in real-time.

## Features ✨

- 📸 Real-time video capture and streaming using OpenCV.
- 🗜️ Efficient video compression with JPEG encoding.
- 📡 UDP-based communication for lightweight and fast data transfer.
- 🏗️ Modular client-server architecture.

## Requirements 📋

To run this project, ensure you have the following dependencies installed:

```plaintext
numpy==1.24.3
opencv-python
```

You can install the dependencies using:

```bash
pip install -r requirements.txt
```

## Directory Structure 📂

The project directory is organized as follows:

```
OpenCV-streaming/
├── OpenCVClient.py        # Client script for capturing and sending video
├── OpenCVServer.py        # Server script for receiving and displaying video
├── requirements.txt       # Python dependencies
```

## File Descriptions 📂

### 1. `OpenCVClient.py` 🖥️
- Captures video from the webcam.
- Compresses the video frames using JPEG encoding.
- Sends the compressed frames to the server over a UDP socket.

### 2. `OpenCVServer.py` 🖥️
- Receives the video frames from the client.
- Decodes the frames and displays them in real-time.

## How to Run 🚀

### Step 1: Start the Server 🛠️
Run the server script to start listening for incoming video streams:

```bash
python OpenCVServer.py
```

### Step 2: Start the Client 🎥
Run the client script to capture and send video to the server:

```bash
python OpenCVClient.py
```

### Step 3: View the Stream 👀
- The server will display the video stream in a window titled `Img Server`.
- The client will display the video being captured in a window titled `Img Client`.

### Step 4: Stop the Stream ✋
Press the `Esc` key on either the client or server window to stop the video stream and close the application.

## 🧠 How Camera Indexes Work

Each physical or virtual camera connected to your system is assigned an index number, starting from 0:

- `0` → Usually the default built-in webcam
- `1` → An external USB camera (if connected)
- `2, 3, etc.` → Other cameras or virtual video devices

This project uses the following code to access the default camera:

```python
cap = cv2.VideoCapture(0)
```

## Notes 📝

- Ensure both the client and server are running on the same network.
- Update the `server_ip` and `server_port` variables in `OpenCVClient.py` if the server is running on a different machine.

## License 📜

This project is licensed under the MIT License. See [LICENSE](./LICENSE) for details.

## Acknowledgments 🙌

- [OpenCV](https://opencv.org/) for providing powerful computer vision tools.
- Python's built-in libraries for enabling seamless networking and data handling.