

# 📌 ORB-SLAM3

ORB-SLAM3 is a state-of-the-art real-time **Visual SLAM** (Simultaneous Localization and Mapping) system. It supports **monocular, stereo, RGB-D cameras**, and **visual-inertial fusion**, making it highly suitable for robotics, drones, and autonomous systems.

---

## 🔍 Features

* **Real-time tracking**
* **Map creation and optimization**
* **Loop closure detection**
* **Support for multiple sensor setups**

  * Monocular
  * Stereo
  * RGB-D
  * Visual-Inertial (IMU + Camera)
* **Relocalization**
* **Works indoors and outdoors**

---

## 📦 Requirements

* Ubuntu 18.04 / 20.04
* C++17
* OpenCV
* Eigen3
* Pangolin
* Boost
* ROS (optional for ROS integration)

---
## 🎥 Demo Video

Click the image below to watch the demo:

[![Watch Demo](https://img.youtube.com/vi/K-HbNhwnD50/maxresdefault.jpg)](https://www.youtube.com/watch?v=K-HbNhwnD50)


## ⚙️ Installation

### 1. Install dependencies

```bash
sudo apt-get update
sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
sudo apt-get install libeigen3-dev libboost-all-dev
sudo apt-get install libopencv-dev
```

### 2. Clone the repository

```bash
git clone https://github.com/UZ-SLAMLab/ORB_SLAM3.git
cd ORB_SLAM3
```

### 3. Build

```bash
chmod +x build.sh
./build.sh
```

---

## 🚀 Usage

### Monocular

```bash
./Examples/Monocular/mono_tum Vocabulary/ORBvoc.txt Examples/Monocular/TUM1.yaml PATH_TO_SEQUENCE
```

### Stereo

```bash
./Examples/Stereo/stereo_euroc Vocabulary/ORBvoc.txt Examples/Stereo/EuRoC.yaml PATH_TO_SEQUENCE
```

### RGB-D

```bash
./Examples/RGB-D/rgbd_tum Vocabulary/ORBvoc.txt Examples/RGB-D/TUM1.yaml PATH_TO_SEQUENCE
```

---

## 🛰️ Visual-Inertial (IMU) Mode

```bash
./Examples/IMU/mono_inertial Vocabulary/ORBvoc.txt Examples/IMU/EuRoC.yaml PATH_TO_SEQUENCE
```

---

## 📁 Folder Structure

```
ORB_SLAM3/
├── Examples/
├── ORB_SLAM3/
├── Thirdparty/
├── Vocabulary/
├── build/
└── README.md
```

---

## 🧠 How it works (Short Overview)

1. **Extract ORB features** from images
2. **Track keypoints** across frames
3. **Estimate camera pose**
4. **Build 3D map**
5. **Detect loop closure**
6. **Optimize map using bundle adjustment**
