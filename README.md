# vsens-studio

# 羽瞬科技 - 电容型触觉传感器数据采集软件
# Vsens Technology - Capacitive Tactile Sensor Data Acquisition Software

---

## 说明

### 简介
本仓库包含羽瞬科技（深圳）有限公司电容型触觉传感器的上位机软件及驱动。支持24通道数据的实时采集、3D/2D可视化显示及数据录制。

### 安装与运行
1.  **安装驱动**：进入 `CH341SER` 文件夹，运行安装程序安装串口驱动。
2.  **连接设备**：通过 USB 连接传感器，系统将识别为 COM 端口。
3.  **运行软件**：直接运行根目录下的主程序 `.exe` 文件。

### 核心功能与操作
*   **数据采集**：打开软件自动识别串口，点击左上角 **“开始”** 即可采集。
*   **基准校准**：在无外力状态下，点击 **“设定基面”** 进行零点校准（去除静态底噪）。
*   **可视化**：
    *   **3D图**：显示压力立体分布，支持右键拖动旋转。
    *   **2D热力图**：蓝红渐变色显示压力强度。
*   **数据录制**：点击 **“保存”** 按钮（图标点亮），数据将自动存入软件位置的文件夹。

### 数据输出格式
数据按“记录时间”生成的文件夹归档，包含 `.csv` 数据表和 `.avi` 视频。

**CSV 数据格式：**
`CHxx: Raw=aaaaa (Δ bbb) -> P=c.cc kPa`
*   `CHxx`: 通道编号 (0-23)
*   `Raw`: 原始电容值
*   `Δ`: 变化量
*   `P`: 压强值 (kPa)

---

## Instructions

### Introduction
This repository contains the host software and drivers for Vsens Technology's capacitive tactile sensors. It supports real-time data acquisition, 3D/2D visualization, and data logging for 24-channel sensors.

### Installation & Setup
1.  **Install Driver**: Navigate to the `CH341SER` folder and run the installer for the serial driver.
2.  **Connect Device**: Connect the sensor via USB. It will be recognized as a COM port.
3.  **Run Software**: Execute the main `.exe` file in the root directory.

### Key Features & Usage
*   **Acquisition**: The software auto-detects the COM port. Click **"Start"** to begin.
*   **Calibration**: With no pressure applied, click **"Set Baseline"** to zero out static noise.
*   **Visualization**:
    *   **3D Plot**: Shows pressure distribution; supports rotation via right-click.
    *   **2D Heatmap**: Indicates pressure intensity (Blue to Red).
*   **Data Logging**: Toggle the **"Save"** button (icon lights up) to record data to the local folder.

### Data Output
Data is saved in timestamped folders containing `.csv` logs and `.avi` videos.

**CSV Data Format:**
`CHxx: Raw=aaaaa (Δ bbb) -> P=c.cc kPa`
*   `CHxx`: Channel Index (0-23)
*   `Raw`: Raw Capacitance Value
*   `Δ`: Delta Value (Change)
*   `P`: Pressure (kPa)
