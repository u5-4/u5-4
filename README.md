<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,45:2563EB,100:22D3EE&height=230&section=header&text=neck_deep%20%7C%20u5-4&fontSize=44&fontColor=FFFFFF&animation=fadeIn&fontAlignY=35&desc=Robot%20Navigation%20%7C%20UAV%20%2B%20Robot%20Dog%20%2B%20SLAM&descSize=18&descAlignY=55" alt="header" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=700&size=24&pause=800&color=22D3EE&center=true&vCenter=true&width=900&lines=%F0%9F%9A%80+Robot+navigation+launch+sequence;%F0%9F%9B%B8+UAV:+PX4+%2B+MAVROS+%2B+autonomous+mission;%F0%9F%A6%BE+Robot+dog:+Go2+%2B+Hesai+XT-16+%2B+Super-LIO;%F0%9F%93%A1+LiDAR+%2B+IMU+%2B+vision+for+field+robots" alt="rocket typing effect" />
</p>

<p align="center">
  <a href="https://github.com/u5-4"><img src="https://komarev.com/ghpvc/?username=u5-4&style=for-the-badge&color=0ea5e9&label=PROFILE+VIEWS" alt="profile views" /></a>
  <a href="https://github.com/u5-4?tab=repositories"><img src="https://img.shields.io/badge/Public%20Repos-9-22D3EE?style=for-the-badge&logo=github&logoColor=white" alt="public repos" /></a>
  <img src="https://img.shields.io/badge/Main%20Direction-Robot%20Navigation-F97316?style=for-the-badge&logo=rocket&logoColor=white" alt="main direction" />
</p>

## 👋 Hi, I'm neck_deep

My main direction is **robot navigation**: autonomous UAV missions, robot dog LiDAR/IMU SLAM, PX4/MAVROS control, sensor calibration, and field debugging.

I like turning real hardware work into reusable engineering notes: launch scripts, topic chains, calibration workflows, flight-review checklists, and deployment records that can survive the next field test.

## 🎯 Main Direction

| Track | What I work on | Representative repo |
|---|---|---|
| UAV navigation | PX4/MAVROS control, autonomous mission state machine, target detection, path planning, return and landing flow | [-A-](https://github.com/u5-4/-A-) |
| Robot dog navigation | Unitree Go2, Hesai XT-16 LiDAR, Go2 IMU bridge, ROS1 Noetic, Super-LIO odometry and mapping | [GO2_Hesai](https://github.com/u5-4/GO2_Hesai) |
| Perception and calibration | Fisheye camera calibration, Kalibr/TartanCalib, camera geometry, 3D reconstruction notes | [J200-Fisheye-Calibration-Startup](https://github.com/u5-4/J200-Fisheye-Calibration-Startup), [computer-vision-notes](https://github.com/u5-4/computer-vision-notes) |

## 🚀 Mission Control

```text
Core Field    : Robot Navigation
UAV Stack     : PX4 + MAVROS + YOLOv8 + path planning + task state machine
Robot Dog     : Unitree Go2 + Hesai XT-16 + Go2 IMU + ROS1 Noetic + Super-LIO
Perception    : LiDAR / IMU / fisheye camera / camera geometry / calibration
Compute       : Jetson / Orin NX / Ubuntu / ROS
Output        : odometry, map, flight logs, reusable deployment notes
```

## 🛠️ Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/ROS1-Noetic-22314E?style=for-the-badge&logo=ros&logoColor=white" alt="ROS1 Noetic" />
  <img src="https://img.shields.io/badge/PX4-111111?style=for-the-badge&logo=drone&logoColor=white" alt="PX4" />
  <img src="https://img.shields.io/badge/MAVROS-2563EB?style=for-the-badge&logo=gnubash&logoColor=white" alt="MAVROS" />
  <img src="https://img.shields.io/badge/Unitree%20Go2-0F172A?style=for-the-badge&logo=linux&logoColor=white" alt="Unitree Go2" />
  <img src="https://img.shields.io/badge/Hesai%20XT--16-0891B2?style=for-the-badge&logo=radar&logoColor=white" alt="Hesai XT-16" />
  <img src="https://img.shields.io/badge/Super--LIO-14B8A6?style=for-the-badge&logo=mapbox&logoColor=white" alt="Super-LIO" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu" />
  <img src="https://img.shields.io/badge/NVIDIA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" alt="NVIDIA" />
</p>

## 🦾 Robot Dog Navigation

The [GO2_Hesai](https://github.com/u5-4/GO2_Hesai) project records a stable navigation and mapping chain for a **Unitree Go2 robot dog** with a **Hesai XT-16 LiDAR** and the Go2 internal IMU.

```text
Hesai XT-16
  -> Hesai ROS Driver
  -> /lidar_points

Go2 internal IMU
  -> Unitree SDK2 DDS rt/lowstate
  -> go2_imu_bridge
  -> /imu/data

/lidar_points + /imu/data
  -> Super-LIO
  -> /lio/odom
  -> /lio/cloud_world
```

This is one of my key robot navigation tracks: sensor time alignment, ROS topic connection, LiDAR/IMU fusion, odometry stability, mapping output, and launch-script automation.

## 🛰️ Featured Projects

| Project | Focus | Notes |
|---|---|---|
| [GO2_Hesai](https://github.com/u5-4/GO2_Hesai) | Robot dog LiDAR/IMU navigation | Unitree Go2 + Hesai XT-16 + Go2 internal IMU + ROS1 Noetic + Super-LIO. Records `/lidar_points`, `/imu/data`, `/lio/odom`, `/lio/cloud_world`, timestamp alignment, launch scripts, and stability checks. |
| [-A-](https://github.com/u5-4/-A-) | UAV autonomous navigation | ROS-based UAV competition project with YOLOv8 perception, grid path planning, task scheduling, MAVROS/PX4 control, return strategy, takeoff, cruising, obstacle avoidance, delivery, and landing. |
| [J200-Fisheye-Calibration-Startup](https://github.com/u5-4/J200-Fisheye-Calibration-Startup) | J200 four-fisheye calibration | End-to-end workflow for rosbag recording, Kalibr calibration, Orin NX parameter deployment, report reading, IMU joint calibration, and troubleshooting. |
| [Ubunth22.4_ROS1_noetic_nvidia](https://github.com/u5-4/Ubunth22.4_ROS1_noetic_nvidia) | Jetson ARM64 ROS1 Noetic | Source-build notes for ROS1 Noetic on Ubuntu 22.04 Jammy / Jetson ARM64, including environment isolation and common problems. |
| [px4-flight-review-full-guide](https://github.com/u5-4/px4-flight-review-full-guide) | PX4 log analysis | Chinese study guide for PX4 Flight Review: PID tracking, vibration, GPS, EKF flags, actuator outputs, estimator health, and flight debugging order. |
| [computer-vision-notes](https://github.com/u5-4/computer-vision-notes) | 3D reconstruction notes | Camera geometry, single-view geometry, vanishing points, projective transforms, least squares, and the math foundation for calibration / PnP / BA. |
| [3D_Model](https://github.com/u5-4/3D_Model) | SLAM model assets | 3D model drawings for D435I visual SLAM and LiDAR SLAM versions. |
| [tartancalib](https://github.com/u5-4/tartancalib) | Wide-angle calibration | TartanCalib / Kalibr-based wide-angle lens calibration workflow using AprilTags and adaptive subpixel refinement. |

## 🧭 Robotics Pipeline

```mermaid
flowchart LR
    A["UAV Platform<br/>PX4 / MAVROS"] --> C["Robot Navigation Core"]
    B["Robot Dog Platform<br/>Go2 / XT-16 / IMU"] --> C
    C --> D["Perception<br/>YOLOv8 / LiDAR / Camera Geometry"]
    C --> E["Localization & Mapping<br/>Super-LIO / SLAM / Odometry"]
    D --> F["Planning<br/>Grid Path / Replanning / Safety Distance"]
    E --> F
    F --> G["Control<br/>Mission State Machine / Return / Landing"]
    G --> H["Review<br/>Flight Logs / ROS Bags / Debug Notes"]
    H --> C
```

## 📡 Current Orbit

- Focusing on **robot navigation** across UAVs and robot dogs.
- Building reliable **ROS deployment records** for real robotics hardware.
- Connecting **Hesai XT-16 + Go2 IMU + Super-LIO** for robot dog odometry and mapping.
- Organizing **PX4 Flight Review** knowledge into practical UAV debugging checklists.
- Studying **computer vision / 3D reconstruction** from geometry to optimization.

## 📊 GitHub Telemetry

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=u5-4&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=u5-4&layout=compact&theme=tokyonight&hide_border=true" alt="Top languages" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=u5-4&theme=react-dark&hide_border=true&area=true&custom_title=Launch%20Trajectory" alt="activity graph" />
</p>

## 🧩 Pinned Launch Modules

<p align="center">
  <a href="https://github.com/u5-4/GO2_Hesai">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=u5-4&repo=GO2_Hesai&theme=tokyonight&hide_border=true" alt="GO2_Hesai" />
  </a>
  <a href="https://github.com/u5-4/-A-">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=u5-4&repo=-A-&theme=tokyonight&hide_border=true" alt="-A-" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/u5-4/px4-flight-review-full-guide">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=u5-4&repo=px4-flight-review-full-guide&theme=tokyonight&hide_border=true" alt="px4-flight-review-full-guide" />
  </a>
  <a href="https://github.com/u5-4/computer-vision-notes">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=u5-4&repo=computer-vision-notes&theme=tokyonight&hide_border=true" alt="computer-vision-notes" />
  </a>
</p>

## 🔭 Motto

> Build it, fly it, log it, debug it, document it, launch again.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:22D3EE,50:2563EB,100:0F172A&height=120&section=footer" alt="footer" />
</p>
