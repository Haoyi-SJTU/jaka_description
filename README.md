# JAKA Minicobo 机械臂 URDF 模型

本项目提供了 **JAKA Minicob 机械臂** 的完整 ROS 模型描述包，支持在 RVIZ 和 Gazebo 环境中进行可视化、运动规划及仿真测试。模型包含精确的机械结构、真实碰撞体积以及关节实际运动范围，适用于机器人开发、算法验证及教学演示等场景。

![](https://github.com/Haoyi-SJTU/jaka_description/blob/master/fig/2.jpg)
![](https://github.com/Haoyi-SJTU/jaka_description/blob/master/fig/4.jpg)

## 特性

- **高精度机械模型** - 基于真实机械臂尺寸建模
- **真实碰撞体积** - 支持碰撞检测与避障规划
- **关节运动范围** - 包含各关节的实际限位参数
- **双环境支持** - 兼容 RVIZ 可视化与 Gazebo 仿真

## 系统要求

| 组件 | 要求 |
|------|------|
| 操作系统 | 不低于Ubuntu 22.04 |
| 机器人框架 | ROS (Noetic/Humble) |
| 可视化工具 | RVIZ |
| 仿真工具 | Gazebo |

---

##  安装与使用

### 1. 克隆项目

```bash
cd ~/catkin_ws/src
git clone https://github.com/Haoyi-SJTU/jaka_description
cd ..
catkin_make
source devel/setup.bash
```

### 2. 启动 RVIZ 可视化

在终端中运行以下命令，启动 RVIZ 查看机械臂模型，并通过滑块交互移动机器人：

```bash
roslaunch jaka_description display.launch
```

### 3. 启动 Gazebo 仿真

在终端中运行以下命令，在仿真环境中查看和测试机械臂模型：

```bash
roslaunch jaka_description gazebo.launch
```

---

##  项目结构

```
jaka_description/
├── launch/
│   ├── display.launch      # RVIZ 启动文件
│   └── gazebo.launch       # Gazebo 启动文件
├── meshes/                 # 机械臂模型网格文件
├── urdf/                   # URDF 模型描述文件
├── config/                 # 配置文件
├── CMakeLists.txt
└── package.xml
```



## 注意事项

1. 确保 ROS 环境已正确配置并 sourced
2. 首次运行前请执行 `catkin_make` 编译工作空间
3. 关节运动范围已限定，请勿超出物理限位
4. 如遇模型加载问题，请检查 mesh 文件路径


## 许可证

本项目采用 MIT 许可证，详见 [LICENSE](https://github.com/Haoyi-SJTU/jaka_description?tab=MIT-1-ov-file) 文件。

# JAKA Minicobo Robot Arm URDF Model

This project provides a complete ROS model description package for the **JAKA Minicob Robot Arm**, supporting visualization, motion planning, and simulation testing in RVIZ and Gazebo environments. The model includes precise mechanical structures, real collision volumes, and actual joint motion ranges, suitable for scenarios such as robot development, algorithm verification, and teaching demonstrations.

![](https://github.com/Haoyi-SJTU/jaka_description/blob/master/fig/2.jpg)
![](https://github.com/Haoyi-SJTU/jaka_description/blob/master/fig/4.jpg)

## Features

- **High-Precision Mechanical Model** - Modeled based on real robot arm dimensions
- **Real Collision Volumes** - Supports collision detection and obstacle avoidance planning
- **Joint Motion Range** - Includes actual limit parameters for each joint
- **Dual Environment Support** - Compatible with RVIZ visualization and Gazebo simulation

## System Requirements

| Component | Requirements |
|------|------|
| Operating System | Ubuntu 22.04 or higher |
| Robot Framework | ROS (Noetic/Humble) |
| Visualization Tool | RVIZ |
| Simulation Tool | Gazebo |

---

## Installation and Usage

### 1. Clone the Project

```bash
cd ~/catkin_ws/src
git clone https://github.com/Haoyi-SJTU/jaka_description
cd ..
catkin_make
source devel/setup.bash
```

### 2. Launch RVIZ Visualization

Run the following command in the terminal to start RVIZ to view the robot arm model and interactively move the robot via sliders:

```bash
roslaunch jaka_description display.launch
```

### 3. Launch Gazebo Simulation

Run the following command in the terminal to view and test the robot arm model in the simulation environment:

```bash
roslaunch jaka_description gazebo.launch
```

---

## Project Structure

```
jaka_description/
├── launch/
│   ├── display.launch      # RVIZ launch file
│   └── gazebo.launch       # Gazebo launch file
├── meshes/                 # Robot arm model mesh files
├── urdf/                   # URDF model description files
├── config/                 # Configuration files
├── CMakeLists.txt
└── package.xml
```

## Notes

1. Ensure the ROS environment is correctly configured and sourced.
2. Execute `catkin_make` to compile the workspace before the first run.
3. Joint motion ranges are limited; please do not exceed physical limits.
4. If you encounter model loading issues, please check the mesh file paths.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Haoyi-SJTU/jaka_description?tab=MIT-1-ov-file) file for details.
