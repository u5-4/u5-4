```markdown
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:020617,30:0F172A,55:2563EB,80:22D3EE,100:F97316&height=260&section=header&text=neck_deep%20%7C%20u5-4&fontSize=46&fontColor=FFFFFF&animation=fadeIn&fontAlignY=34&desc=Robot%20Navigation%20%7C%20UAV%20Autonomy%20%7C%20Go2%20SLAM%20%7C%20Field%20Robotics&descSize=18&descAlignY=55" alt="header" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=800&size=24&pause=700&color=22D3EE&center=true&vCenter=true&width=1000&lines=Initializing+Robot+Navigation+Stack...;PX4+%2B+MAVROS+%2B+Autonomous+UAV+Mission;Unitree+Go2+%2B+Hesai+XT-16+%2B+Super-LIO;LiDAR+%2B+IMU+%2B+Vision+%3D+Field+Robotics;Build+it.+Fly+it.+Log+it.+Debug+it.+Launch+again." alt="typing animation" />
</p>

<p align="center">
  <a href="https://github.com/u5-4">
    <img src="https://komarev.com/ghpvc/?username=u5-4&style=for-the-badge&color=22D3EE&label=PROFILE+VIEWS" alt="profile views" />
  </a>
  <a href="https://github.com/u5-4?tab=repositories">
    <img src="https://img.shields.io/badge/Public%20Repos-Robotics%20Lab-0EA5E9?style=for-the-badge&logo=github&logoColor=white" alt="repos" />
  </a>
  <img src="https://img.shields.io/badge/Main%20Direction-Robot%20Navigation-F97316?style=for-the-badge&logo=rocket&logoColor=white" alt="main direction" />
  <img src="https://img.shields.io/badge/Style-Cyberpunk%20Field%20Engineering-A855F7?style=for-the-badge&logo=gnometerminal&logoColor=white" alt="style" />
</p>

---

## Hi, I'm `neck_deep`

我主要做 **机器人导航与多传感器工程部署**，方向集中在：

- **无人机自主飞行**：PX4、MAVROS、任务状态机、路径规划、目标识别、返航与降落。
- **四足机器人 SLAM / Navigation**：Unitree Go2、Hesai XT-16、Go2 内部 IMU、ROS1 Noetic、Super-LIO。
- **感知与标定**：鱼眼相机、Kalibr / TartanCalib、相机几何、3D reconstruction、LiDAR / IMU 时间同步。
- **真实硬件调试**：Jetson / Orin NX、Ubuntu、ROS 环境、驱动编译、日志分析、现场部署文档。

我的定位不是只写算法 demo，而是把算法、传感器、机器人本体、网络、时间戳、ROS 话题、启动脚本和调试记录连成能跑起来的系统。

---

## Navigation Console

```text
CALLSIGN       : neck_deep / u5-4
MAIN FIELD     : Robot Navigation & Field Robotics
UAV STACK      : PX4 + MAVROS + YOLOv8 + Path Planning + Mission FSM
ROBOT DOG      : Unitree Go2 + Hesai XT-16 + Go2 IMU + Super-LIO
PERCEPTION     : LiDAR / IMU / Fisheye Camera / Calibration / Geometry
COMPUTE        : Ubuntu / ROS1 Noetic / Jetson / Orin NX / C++ / Python
OUTPUT         : Odometry / Map / Flight Logs / ROS Bags / Deployment Notes
ENGINEERING    : Build -> Test -> Log -> Debug -> Document -> Relaunch
```

---

## Core Tracks

| Track | What I build | Representative Repos |
|---|---|---|
| UAV Autonomous Navigation | 无人机任务流程、路径规划、避障、目标识别、PX4/MAVROS 控制、返航与降落 | [`-A-`](https://github.com/u5-4/-A-), [`px4-flight-review-full-guide`](https://github.com/u5-4/px4-flight-review-full-guide) |
| Robot Dog SLAM | Go2 四足机器人外接 Hesai XT-16，融合 Go2 内部 IMU，跑 Super-LIO 定位建图 | [`GO2_Hesai`](https://github.com/u5-4/GO2_Hesai) |
| Sensor Calibration | J200 / 鱼眼相机 / Kalibr / TartanCalib / AprilTag / 相机与 IMU 标定 | [`J200-Fisheye-Calibration-Startup`](https://github.com/u5-4/J200-Fisheye-Calibration-Startup), [`tartancalib`](https://github.com/u5-4/tartancalib) |
| Vision Geometry | 计算机视觉、相机模型、单视图几何、消失点、PnP、3D reconstruction 基础 | [`computer-vision-notes`](https://github.com/u5-4/computer-vision-notes) |
| Deployment Notes | Jetson / Ubuntu / ROS1 Noetic / NVIDIA 环境编译与部署记录 | [`Ubunth22.4_ROS1_noetic_nvidia`](https://github.com/u5-4/Ubunth22.4_ROS1_noetic_nvidia) |
| Model Assets | D435I / LiDAR SLAM 相关 3D 模型与工程素材 | [`3D_Model`](https://github.com/u5-4/3D_Model) |

---

## Featured Project: Go2 + Hesai XT-16 + Super-LIO

[`GO2_Hesai`](https://github.com/u5-4/GO2_Hesai) 是我当前四足机器人导航方向的核心工程之一。

```text
Hesai XT-16
    -> hesai_ros_driver
    -> /lidar_points

Go2 Internal IMU
    -> Unitree SDK2 / DDS / rt/lowstate
    -> go2_imu_bridge
    -> /imu/data

/lidar_points + /imu/data
    -> Super-LIO
    -> /lio/odom
    -> /lio/cloud_world
```

这个仓库重点记录：

- Hesai XT-16 网络参数、端口、点云话题配置。
- Go2 内部 IMU 通过 Unitree SDK2 / DDS 转 ROS1 `/imu/data`。
- LiDAR 与 IMU 时间戳对齐。
- Super-LIO 参数、外参、重力模长、话题配置。
- 一键启动脚本与定位结果检查命令。
- 从驱动、话题、时间同步到 SLAM 输出的完整部署链路。

---

## Featured Project: UAV Autonomous Mission

[`-A-`](https://github.com/u5-4/-A-) 面向无人机自主飞行任务，核心目标是让无人机在已知或动态变化环境中安全完成任务。

主要模块包括：

- 地图 / 栅格 / 航点输入。
- 障碍物检测与安全距离约束。
- 路径规划与实时重规划。
- 速度、姿态、航向控制指令输出。
- 起飞、巡航、绕障、到点悬停、返航、降落任务流程。
- YOLOv8 视觉识别与任务状态机结合。
- PX4 / MAVROS 调试与飞行日志分析。

---

## Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=cpp,python,linux,ubuntu,ros,opencv,git,github,bash,cmake,vscode" alt="skill icons" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/C++-Robot%20Runtime-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-Tools%20%26%20Scripts-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/ROS1-Noetic-22314E?style=for-the-badge&logo=ros&logoColor=white" />
  <img src="https://img.shields.io/badge/PX4-Flight%20Control-111111?style=for-the-badge&logo=drone&logoColor=white" />
  <img src="https://img.shields.io/badge/MAVROS-UAV%20Bridge-2563EB?style=for-the-badge&logo=gnubash&logoColor=white" />
  <img src="https://img.shields.io/badge/Unitree%20Go2-Quadruped-0F172A?style=for-the-badge&logo=linux&logoColor=white" />
  <img src="https://img.shields.io/badge/Hesai%20XT--16-LiDAR-06B6D4?style=for-the-badge&logo=radar&logoColor=white" />
  <img src="https://img.shields.io/badge/Super--LIO-LiDAR%20Inertial%20Odometry-14B8A6?style=for-the-badge&logo=mapbox&logoColor=white" />
  <img src="https://img.shields.io/badge/NVIDIA-Jetson%20%2F%20Orin-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
</p>

---

## System Map

```mermaid
flowchart LR
    A["UAV Platform<br/>PX4 / MAVROS"] --> C["Robot Navigation Core"]
    B["Robot Dog Platform<br/>Go2 / Hesai XT-16 / IMU"] --> C
    D["Sensor Calibration<br/>Kalibr / TartanCalib / Fisheye"] --> C
    C --> E["Perception<br/>YOLOv8 / LiDAR / Camera Geometry"]
    C --> F["Localization & Mapping<br/>Super-LIO / Odometry / Point Cloud Map"]
    E --> G["Planning<br/>Grid Path / Replanning / Safety Distance"]
    F --> G
    G --> H["Control<br/>Mission FSM / Return / Landing"]
    H --> I["Review<br/>PX4 Flight Logs / ROS Bags / Field Notes"]
    I --> C
```

---

## Project Radar

| Repo | Role in My Stack |
|---|---|
| [`GO2_Hesai`](https://github.com/u5-4/GO2_Hesai) | 四足机器人 LiDAR-IMU SLAM 工程链路，Go2 + Hesai XT-16 + Super-LIO。 |
| [`-A-`](https://github.com/u5-4/-A-) | 无人机自主飞行任务核心代码，路径规划、控制、任务状态机与视觉感知。 |
| [`px4-flight-review-full-guide`](https://github.com/u5-4/px4-flight-review-full-guide) | PX4 Flight Review 中文学习与飞行日志诊断笔记。 |
| [`J200-Fisheye-Calibration-Startup`](https://github.com/u5-4/J200-Fisheye-Calibration-Startup) | J200 四鱼眼相机标定、rosbag、Kalibr、Orin NX 参数部署流程。 |
| [`computer-vision-notes`](https://github.com/u5-4/computer-vision-notes) | 计算机视觉与 3D reconstruction 学习笔记。 |
| [`Ubunth22.4_ROS1_noetic_nvidia`](https://github.com/u5-4/Ubunth22.4_ROS1_noetic_nvidia) | Ubuntu 22.04 / Jetson ARM64 / ROS1 Noetic 环境部署记录。 |
| [`3D_Model`](https://github.com/u5-4/3D_Model) | D435I 视觉 SLAM 与 LiDAR SLAM 相关模型素材。 |
| [`tartancalib`](https://github.com/u5-4/tartancalib) | 广角相机标定方向的学习与工具参考。 |

---

## GitHub Telemetry

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=u5-4&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github&include_all_commits=true" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=u5-4&layout=compact&theme=tokyonight&hide_border=true" alt="Top languages" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=u5-4&theme=tokyonight&hide_border=true&mode=weekly" alt="GitHub streak" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=u5-4&theme=react-dark&hide_border=true&area=true&custom_title=Cyberpunk%20Launch%20Trajectory" alt="activity graph" />
</p>

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=u5-4&theme=tokyonight&no-frame=true&no-bg=true&margin-w=8&margin-h=8&column=6" alt="GitHub trophies" />
</p>

---

## Pinned Launch Modules

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

---

## Current Orbit

- 正在强化 **四足机器人 LiDAR-IMU SLAM** 的工程稳定性。
- 持续整理 **PX4 飞行日志分析** 与无人机调参经验。
- 学习并实践 **相机标定、鱼眼模型、3D reconstruction**。
- 把每次真实硬件调试变成可复现的 README、脚本和排错流程。

---

## Motto

> Build it, fly it, log it, debug it, document it, launch again.

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=800&size=20&pause=900&color=F97316&center=true&vCenter=true&width=850&lines=Field+Robotics+is+not+only+algorithm.;It+is+network,+timestamp,+driver,+launch,+and+debug.;When+the+robot+moves,+the+README+must+survive." alt="footer typing" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:F97316,40:22D3EE,70:2563EB,100:020617&height=130&section=footer" alt="footer" />
</p>
```
