![header](https://capsule-render.vercel.app/api?type=rect&color=timeGradient&text=AUTONOMOUS%20VEHICLE%20LOCALIZATION&fontSize=20)

## <div align=center>🎥 DEMO VIDEO</div>
[![Demo Video](https://img.youtube.com/vi/_7AnEae8NlM/maxresdefault.jpg)](https://www.youtube.com/watch?v=_7AnEae8NlM)
*Click the image above to watch the demo video*

## <div align=left>REPO INFO</div>  
- IEEE Transactions on Robotics Research Implementation
- **Autonomous Vehicle Localization Without Prior High-Definition Map**
- ROS1-based Multi-Sensor Fusion System for Autonomous Navigation

## <div align=left>REPO CONFIG</div>  
#### LOCALIZE_PKG  
* NDT-based localization with multi-sensor state estimation
* Real-time pose estimation using point cloud maps
* Integration of wheeled odometry, IMU, and LiDAR
* Robot localization package for continuous global positioning

#### SLAM_PKG  
* **LIO-SAM**: Tightly-coupled LiDAR Inertial Odometry via Smoothing and Mapping
* **SC-LIO-SAM**: Scan Context enhanced LIO-SAM for loop closure
* **GICP-SAM**: Generalized ICP with Smoothing and Mapping
* **GICP-I-SAM**: Incremental GICP-SAM implementation
* **LeGO-LOAM**: Lightweight and Ground-Optimized LiDAR Odometry

#### RESEARCH_PKG  
* **LocalMapping**: VGICP-SAM based local mapping system
* **DatabasePlayer**: Multi-dataset player for KITTI, MulRan, ComplexUrban
* **OSMFusion**: OpenStreetMap integration for route planning

#### SENSORS_PKG  
* Multi-sensor integration including:
  - Camera (BlackFly-S FLIR, Theta V, UMD Camera)
  - IMU (EB-IMU, Xsens MTi Driver)
  - LiDAR (Velodyne, RGB-LiDAR fusion)
  - UWB Radar systems
  - GPS/GNSS sensors

## <div align=left>REPO USE</div> 
<pre>cd catkin_ws/src/  
git clone https://github.com/iismn/IEEE_T-RO_AutonomousVehicleLocalization-without-Prior-HDMap.git  
cd ../.. && catkin_make</pre>

## <div align=left>SYSTEM REQUIREMENTS</div>
#### HARDWARE
- Velodyne VLP-16/VLP-32C LiDAR
- Xsens MTi-670 IMU
- GNSS/GPS Receiver
- Wheeled Odometry Sensors
- Intel Core i7 or equivalent
- NVIDIA GPU (GTX 1060 or higher recommended)

#### SOFTWARE DEPENDENCIES
- Ubuntu 20.04 LTS
- ROS1 Noetic
- PCL 1.10+
- GTSAM 4.0+
- Eigen 3.3+
- OpenCV 4.2+
- robot_localization package

#### DOCKER ENVIRONMENT
Environment is provided via Docker (Ubuntu 20.04 + ROS1)

**Docker Hub Repository:**
```bash
docker pull iismn/environment_tro:LTS20_NV11.3_PyTorch_DL
```
🔗 [Docker Hub Link](https://hub.docker.com/repository/docker/iismn/environment_tro/general)

## <div align=left>ADD INFO</div>
#### AUTONOMOUS VEHICLE SYSTEM COMPONENTS 
- **Multi-Sensor Fusion Architecture**
  - LiDAR-based SLAM and Localization
  - IMU-aided State Estimation
  - GPS/GNSS Global Positioning
  - Wheeled Odometry Integration

- **Advanced Localization Algorithms**
  - NDT (Normal Distributions Transform) Localizer
  - Tightly-coupled LiDAR-Inertial Odometry
  - Scan Context Loop Closure Detection
  - Generalized ICP Registration

- **Research Contributions**
  - Autonomous navigation without prior HD maps
  - Real-time multi-sensor state estimation
  - Robust localization in GPS-denied environments
  - Open-source implementation for research community

#### V 1.0.0 (IEEE T-RO Publication)
- Complete autonomous vehicle localization system
- Multi-dataset validation (KITTI, MulRan, ComplexUrban)
- Real-time performance optimization
- Comprehensive sensor fusion pipeline

#### V 1.1.0 (Planned)
- Enhanced loop closure detection
- Improved computational efficiency
- Additional dataset support
- Extended documentation and tutorials

## <div align=left>LAUNCH INSTRUCTIONS</div>
#### NDT Localization System
<pre>roslaunch ndt_localizer ndt_localizer.launch</pre>

#### LIO-SAM SLAM System  
<pre>roslaunch lio_sam run.launch</pre>

#### SC-LIO-SAM with Loop Closure
<pre>roslaunch sc_lio_sam run.launch</pre>

#### GICP-SAM Mapping System
<pre>roslaunch agv_global_module run.launch</pre>

#### Local Mapping System
<pre>roslaunch agv_local_module run.launch</pre>

#### Complete Mission Pipeline
<pre># Terminal 1: Start sensors
roslaunch sensors_pkg sensor_fusion.launch

# Terminal 2: Start SLAM
roslaunch lio_sam run.launch

# Terminal 3: Start localization
roslaunch ndt_localizer ndt_localizer.launch

# Terminal 4: Start local mapping
roslaunch agv_local_module run.launch</pre>

## <div align=left>CITATION</div>
If you use this code for your research, please cite our paper:

```bibtex
@article{lee2024autonomous,
  title={Autonomous Vehicle Localization Without Prior High-Definition Map},
  author={Lee, Sangmin and Ryu, Jee-Hwan},
  journal={IEEE Transactions on Robotics},
  volume={40},
  pages={2888--2906},
  year={2024},
  doi={10.1109/TRO.2024.3392149},
  publisher={IEEE}
}
```

## <div align=left>ACKNOWLEDGMENTS</div>
- [LIO-SAM](https://github.com/TixiaoShan/LIO-SAM) - Tixiao Shan, Brendan Englot
- [SC-LIO-SAM](https://github.com/gisbi-kim/SC-LIO-SAM) - Giseop Kim
- [LeGO-LOAM](https://github.com/RobustFieldAutonomyLab/LeGO-LOAM) - Tixiao Shan, Brendan Englot
- [NDT Localizer](https://github.com/FAIRSpace-AdMaLL/ndt_localizer) - FAIRSpace-AdMaLL
- [Robot Localization](http://docs.ros.org/en/melodic/api/robot_localization/html/index.html) - Tom Moore

## <div align=left>LICENSE</div>
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## <div align=left>CONTACT</div>
- **Author**: Sangmin Lee, Jee-Hwan Ryu
- **Institution**: Korea Advanced Institute of Science and Technology (KAIST)
- **Email**: [Contact Information]
- **Paper**: [IEEE Xplore](https://doi.org/10.1109/TRO.2024.3392149)

---
**Keywords**: Autonomous vehicle navigation, localization, place recognition (PR), simultaneous localization and mapping (SLAM)
