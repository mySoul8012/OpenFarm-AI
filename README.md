
# OpenFarm AI
### 基于米家生态的企业级 AI 智能农业水培系统
### Enterprise AI-Powered Smart Hydroponics System Based on the Xiaomi Mi Home Ecosystem

> 让农业智能化，让种植自动化，让每个空间都成为智能农场。
>
> Making Agriculture Intelligent, Growing Automated, and Every Space a Smart Farm.

---

## 1. 项目简介 | Introduction

**中文**

OpenFarm AI 是一个面向家庭、企业、实验室、学校及商业农业场景的开源智能水培项目。

项目以小米米家生态（Xiaomi Mi Home）和 Home Assistant 为智能设备管理基础，结合自主研发的农业控制器、PCB 电路板、环境传感器、供水系统、加热系统及人工智能技术，构建一套模块化、自动化、可扩展的智能农业基础设施。

项目不仅关注植物种植本身，也关注水、电、温度、光照、营养液、环境监测和设备控制等完整农业基础设施，致力于打造一套从家庭水培到企业级室内农业均可扩展的智能农业平台。

**English**

OpenFarm AI is an open-source smart hydroponics project designed for homes, businesses, laboratories, schools, and commercial agricultural environments.

Built around the Xiaomi Mi Home ecosystem and Home Assistant, the project integrates custom agricultural controllers, PCB designs, environmental sensors, water circulation systems, heating systems, and artificial intelligence technologies to create a modular, automated, and scalable smart farming infrastructure.

Beyond plant cultivation, OpenFarm AI addresses the complete agricultural infrastructure, including water management, electrical systems, temperature regulation, lighting, nutrient solutions, environmental monitoring, and automated equipment control.

Our goal is to build an extensible intelligent agriculture platform, from home hydroponics to enterprise-scale indoor farming.

---

## 2. 项目目标 | Project Goals

**中文**

- 建立基于米家生态的智能农业设备管理系统。
- 实现水培环境的自动监测与自动控制。
- 自主设计农业控制器、电路板及 PCB。
- 建立模块化供水、循环、排水及营养液管理系统。
- 实现温度、湿度、水位、pH、EC 等参数监测。
- 集成补光、加热、通风、灌溉等自动化设备。
- 引入 AI 视觉识别和智能种植管理能力。
- 提供开放的硬件设计、软件代码、设备接口和部署方案。

**English**

- Build a smart agricultural device management system based on the Xiaomi ecosystem.
- Enable automated monitoring and control of hydroponic environments.
- Develop custom agricultural controllers, circuit boards, and PCB designs.
- Build modular water supply, circulation, drainage, and nutrient management systems.
- Monitor temperature, humidity, water levels, pH, and EC.
- Integrate automated lighting, heating, ventilation, and irrigation.
- Introduce AI-powered visual recognition and intelligent crop management.
- Provide open hardware designs, software, device interfaces, and deployment solutions.

---

## 3. 系统总体架构 | System Architecture

OpenFarm AI 采用软硬件分离、模块化设计。

OpenFarm AI adopts a modular architecture with separated hardware and software layers.

```text
                      OpenFarm AI
                           |
              +------------+------------+
              |                         |
          AI 智能平台                 设备管理平台
          AI Platform             Device Management
              |                         |
       植物视觉识别                 Home Assistant
       Plant Recognition                |
       生长状态分析                 Xiaomi Mi Home
       Growth Analysis                  |
       种植建议                    MQTT / ESPHome
       Growing Recommendations          |
       AI Control Agent                 |
              |                         |
              +------------+------------+
                           |
                    农业控制系统
                 Agricultural Control
                           |
          +----------------+----------------+
          |                |                |
       传感器系统       执行器系统        基础设施
       Sensors         Actuators       Infrastructure
          |                |                |
       pH / EC          水泵 / 阀门       水管 / 水箱
       Temperature      Pumps / Valves    Pipes / Tanks
       Humidity         补光灯            Heating
       Water Level      Grow Lights       Growing Systems
       Light            Fans              Drainage
```

---

## 4. 硬件系统 | Hardware Systems

### 4.1 主控电路板与 PCB 设计 | Controller & PCB Design

**中文**

自主设计 OpenFarm AI 农业控制器，负责传感器数据采集、设备控制和通信。

计划包含：

- ESP32 主控模块。
- 传感器信号采集电路。
- pH 和 EC 传感器接口。
- 水温、空气温湿度传感器接口。
- 水位及液位检测接口。
- 水泵、风扇、电磁阀控制接口。
- 补光灯及加热设备控制接口。
- 继电器或 MOSFET 驱动模块。
- 电源管理及过流保护。
- Wi-Fi、蓝牙及 MQTT 通信支持。
- 状态指示灯、调试接口及扩展接口。

PCB 设计计划公开：

- 原理图（Schematic）。
- PCB Layout。
- Gerber 制造文件。
- BOM 元器件清单。
- 3D PCB 模型。
- 接线图及硬件说明。
- 固件及烧录说明。

**English**

OpenFarm AI aims to develop custom agricultural controllers for sensor acquisition, equipment control, and communication.

Planned hardware features:

- ESP32 main controller.
- Sensor signal acquisition circuits.
- pH and EC sensor interfaces.
- Water temperature and ambient temperature/humidity interfaces.
- Water level detection interfaces.
- Pump, fan, and solenoid valve control interfaces.
- Grow light and heating control interfaces.
- Relay and MOSFET driver modules.
- Power management and overcurrent protection.
- Wi-Fi, Bluetooth, and MQTT connectivity.
- Status indicators, debugging ports, and expansion interfaces.

Planned open hardware deliverables:

- Electrical schematics.
- PCB layout files.
- Gerber manufacturing files.
- Bill of Materials (BOM).
- 3D PCB models.
- Wiring diagrams and hardware documentation.
- Firmware and flashing instructions.

### 4.2 传感器系统 | Sensor Systems

用于持续监测植物生长环境和水培系统运行状态。

Continuous monitoring of growing conditions and hydroponic system performance.

| 监测项目 / Parameter | 主要用途 / Purpose |
|---|---|
| 空气温度 / Air Temperature | 监测种植环境温度 / Monitor ambient temperature |
| 空气湿度 / Air Humidity | 监测空气湿度 / Monitor humidity |
| 水温 / Water Temperature | 监测营养液温度 / Monitor nutrient solution temperature |
| pH | 监测营养液酸碱度 / Monitor acidity and alkalinity |
| EC | 监测营养液电导率 / Monitor electrical conductivity |
| 水位 / Water Level | 监测水箱液位 / Monitor tank levels |
| 光照 / Light Intensity | 调节植物补光 / Control grow lighting |
| 水流 / Water Flow | 监测水循环状态 / Monitor circulation |
| 漏水 / Leak Detection | 监测管路及设备漏水 / Detect water leaks |
| 摄像头 / Camera | 植物生长图像采集 / Capture plant growth images |

### 4.3 水培与供水系统 | Hydroponics & Water Management

**中文**

设计模块化水培基础设施，支持不同规模的种植架和栽培设备。

主要设施：

- 原水储水箱。
- 营养液混合箱。
- 水培栽培槽及种植塔。
- PVC、PE 或食品接触级管路。
- 供水管、回水管及排水管。
- 循环水泵及供水泵。
- 电磁阀及流量控制装置。
- 过滤器及管路接头。
- 水位检测及防溢流设施。
- 自动补水及营养液循环系统。

系统支持循环供水、定时灌溉、自动排水及异常报警。

**English**

The modular hydroponic infrastructure is designed to support different growing configurations and scales.

Planned components:

- Fresh water storage tanks.
- Nutrient solution mixing tanks.
- Hydroponic growing channels and towers.
- PVC, PE, or food-contact-rated piping.
- Water supply, return, and drainage pipes.
- Circulation pumps and water supply pumps.
- Solenoid valves and flow control devices.
- Filters and pipe fittings.
- Water level monitoring and overflow protection.
- Automatic water replenishment and nutrient circulation.

The system is designed to support recirculating water supply, scheduled irrigation, automatic drainage, and fault notifications.

### 4.4 温度控制与加热设施 | Temperature Control & Heating

**中文**

根据不同植物和种植环境配置温度控制设备。

计划支持：

- 电热毯及育苗加热垫。
- 水箱及营养液加热器。
- 根系区域加热设施。
- 温度传感器及温控模块。
- 保温棉及隔热材料。
- 环境通风及散热风扇。
- 自动温度控制与超温报警。

加热设备应使用符合当地规范的产品，并配置独立温控、过温保护及漏电保护。电热毯等设备需与水源隔离，避免直接接触水体。

**English**

Temperature control equipment will be configured according to different plant species and growing environments.

Planned components:

- Electric heating blankets and seedling heat mats.
- Water tank and nutrient solution heaters.
- Root-zone heating systems.
- Temperature sensors and thermostat modules.
- Thermal insulation materials.
- Ventilation and cooling fans.
- Automatic temperature regulation and overtemperature alarms.

Heating equipment must comply with applicable local electrical and safety standards. Independent temperature control, overtemperature protection, and ground-fault protection are required. Heating mats must be isolated from water sources.

### 4.5 光照与环境控制 | Lighting & Environmental Control

**中文**

- LED 全光谱植物生长灯。
- 自动补光控制。
- 光照强度监测。
- 自动通风系统。
- 空气循环风扇。
- 湿度控制设备。
- 温湿度联动控制。

**English**

- Full-spectrum LED grow lights.
- Automated lighting control.
- Light intensity monitoring.
- Automated ventilation.
- Air circulation fans.
- Humidity control equipment.
- Integrated temperature and humidity automation.

---

## 5. 软件与智能平台 | Software & Intelligence Platform

### Home Assistant

**中文：** 作为统一设备管理和自动化平台，接入米家设备及自主研发的农业硬件。

**English:** Serves as the central device management and automation platform, connecting Xiaomi devices and custom agricultural hardware.

### Xiaomi Mi Home Ecosystem

**中文：** 通过支持的米家设备和 Home Assistant 集成，实现温湿度监测、智能插座控制及其他设备联动。

说明：米家设备接入 Home Assistant，不等于自研硬件已经获得米家 App 原生接入能力。后续可根据小米 IoT 平台的接入条件探索原生生态集成。

**English:** Supported Xiaomi Mi Home devices can be integrated through Home Assistant for environmental monitoring, smart plug control, and device automation.

Note: Integrating Xiaomi devices with Home Assistant does not automatically make custom hardware natively compatible with the Mi Home app. Native integration may be explored subject to Xiaomi IoT platform requirements.

### ESP32 / ESPHome

**中文：** 用于农业控制器固件开发、传感器数据采集和执行器控制。

**English:** Used for agricultural controller firmware development, sensor data acquisition, and actuator control.

### MQTT

**中文：** 用于农业设备、Home Assistant 和 AI 平台之间的数据通信。

**English:** Provides messaging and data communication between agricultural devices, Home Assistant, and the AI platform.

### AI 智能系统 | AI Intelligence

**中文**

计划开发：

- AI 植物生长状态识别。
- 植物病害及异常识别。
- 生长周期记录与分析。
- pH、EC 及环境数据分析。
- 智能补光和温度调节建议。
- 自动灌溉及营养液管理策略。
- AI 种植助手及设备控制 Agent。

AI 自动控制将结合设备权限、运行规则和安全阈值，避免模型直接执行不受约束的设备操作。

**English**

Planned AI capabilities:

- AI-powered plant growth recognition.
- Plant disease and anomaly detection.
- Growth cycle tracking and analysis.
- pH, EC, and environmental data analysis.
- Intelligent lighting and temperature recommendations.
- Automated irrigation and nutrient management strategies.
- AI growing assistant and equipment control agent.

AI-driven automation will operate within defined permissions, operational rules, and safety thresholds to prevent unrestricted equipment control.

---

## 6. 农业基础设施 | Agricultural Infrastructure

项目支持从单个水培设备到多区域农业设施的扩展。

Designed to scale from individual hydroponic units to multi-zone agricultural facilities.

| 基础设施 / Infrastructure | 功能 / Function |
|---|---|
| 水培种植架 / Growing Racks | 支撑植物及栽培模块 / Support plants and growing modules |
| 储水设施 / Water Storage | 储存原水及营养液 / Store water and nutrients |
| 水循环管路 / Water Circulation | 实现循环供水 / Enable recirculating water |
| 排水设施 / Drainage | 处理废水及设备排水 / Manage wastewater and drainage |
| 电源系统 / Power System | 为农业设备供电 / Supply power to equipment |
| 电气控制箱 / Electrical Control Cabinet | 集中管理供电与控制 / Centralized power and control |
| 加热设施 / Heating | 维持适宜温度 / Maintain suitable temperatures |
| 补光设施 / Grow Lighting | 提供植物生长光照 / Provide supplemental lighting |
| 通风设施 / Ventilation | 调节空气流动 / Regulate airflow |
| 网络设施 / Networking | 连接农业设备及服务器 / Connect devices and servers |
| 摄像头设施 / Cameras | 采集植物生长数据 / Capture plant growth data |

---

## 7. 安全设计 | Safety & Protection

**中文**

农业设施涉及水、电、加热和自动化设备，系统设计需要考虑：

- 强弱电分离。
- 电源过流、短路及过温保护。
- 漏电保护和可靠接地。
- 水泵空转保护。
- 水箱溢流及缺水保护。
- 管路漏水检测。
- 加热设备独立温控。
- 设备故障报警及紧急停止。
- 关键设备支持手动控制。
- 传感器异常时进入安全状态。

涉及市电的 PCB、继电器及控制箱设计，应由具备相应资质的人员进行设计、安装和验证。

**English**

Because agricultural systems involve water, electricity, heating, and automated machinery, safety is a core design requirement.

Key safety considerations:

- Separation of high-voltage and low-voltage circuits.
- Overcurrent, short-circuit, and overtemperature protection.
- Ground-fault protection and proper grounding.
- Dry-run protection for water pumps.
- Tank overflow and low-water protection.
- Water leak detection.
- Independent temperature control for heating equipment.
- Equipment fault alarms and emergency shutdown.
- Manual override for critical equipment.
- Safe-state operation when sensors fail.

PCB designs, electrical enclosures, relays, and mains-powered equipment must be designed, installed, and validated by appropriately qualified personnel.

---

## 8. 项目目录规划 | Repository Structure

```text
OpenFarm-AI/
│
├── README.md
│
├── hardware/
│   ├── controller/
│   │   ├── schematic/
│   │   ├── pcb/
│   │   ├── gerber/
│   │   └── bom/
│   │
│   ├── sensors/
│   ├── power-control/
│   └── enclosure/
│
├── firmware/
│   ├── esp32/
│   └── esphome/
│
├── software/
│   ├── home-assistant/
│   ├── mqtt/
│   ├── backend/
│   └── frontend/
│
├── ai/
│   ├── plant-recognition/
│   ├── data-analysis/
│   └── ai-agent/
│
├── infrastructure/
│   ├── hydroponics/
│   ├── water-pipeline/
│   ├── heating/
│   ├── lighting/
│   └── ventilation/
│
├── docs/
│   ├── installation/
│   ├── wiring/
│   ├── deployment/
│   └── operation/
│
└── LICENSES.md
```

---

## 9. 研发路线 | Development Roadmap

### 第一阶段：基础水培设施
### Phase 1: Basic Hydroponic Infrastructure

**中文**

- 完成水箱、管路、种植架及循环系统设计。
- 完成 ESP32 基础控制器。
- 接入温湿度、水温及水位传感器。

**English**

- Design water tanks, piping, growing racks, and circulation systems.
- Develop the basic ESP32 controller.
- Integrate temperature, humidity, water temperature, and water level sensors.

### 第二阶段：智能设备联动
### Phase 2: Smart Device Integration

**中文**

- 部署 Home Assistant。
- 接入米家智能设备。
- 实现水泵、补光灯和加热设备自动控制。
- 建立设备监控 Dashboard。

**English**

- Deploy Home Assistant.
- Integrate Xiaomi Mi Home smart devices.
- Implement automated control of pumps, grow lights, and heating equipment.
- Build a centralized device monitoring dashboard.

### 第三阶段：农业监测与自动化
### Phase 3: Agricultural Monitoring & Automation

**中文**

- 接入 pH、EC 传感器。
- 实现营养液监测及自动补水。
- 完成温度、光照和灌溉自动化策略。

**English**

- Integrate pH and EC sensors.
- Implement nutrient solution monitoring and automatic water replenishment.
- Develop automated temperature, lighting, and irrigation strategies.

### 第四阶段：AI 智能农业
### Phase 4: AI-Powered Smart Agriculture

**中文**

- 建立植物图像采集系统。
- 开发 AI 植物识别及生长分析。
- 开发 AI 种植助手。
- 实现受安全规则约束的 AI 自动控制。

**English**

- Build a plant image acquisition system.
- Develop AI plant recognition and growth analysis.
- Develop an AI-powered growing assistant.
- Implement AI automation under defined safety constraints.

### 第五阶段：企业级扩展
### Phase 5: Enterprise-Scale Expansion

**中文**

- 支持多种植区域管理。
- 支持多套水培设备集中控制。
- 建立数据记录、报表及告警系统。
- 支持远程运维和设备状态监控。
- 探索商业化农业设备及解决方案。

**English**

- Support multi-zone growing management.
- Enable centralized control of multiple hydroponic systems.
- Develop data logging, reporting, and alerting systems.
- Support remote maintenance and equipment monitoring.
- Explore commercial agricultural equipment and integrated solutions.

---

## 10. 商业化方向 | Commercial Opportunities

**中文**

OpenFarm AI 采用开放平台与商业硬件相结合的模式。

- 智能水培设备及种植系统。
- ESP32 农业控制器及 PCB 模块。
- pH、EC 和环境监测模块。
- 自动营养液管理设备。
- AI 植物识别及种植管理服务。
- 学校、办公室及企业农业解决方案。
- 水培耗材、营养液及替换配件。

**English**

OpenFarm AI combines an open technology platform with commercial hardware and services.

- Smart hydroponic equipment and growing systems.
- ESP32 agricultural controllers and PCB modules.
- pH, EC, and environmental monitoring modules.
- Automated nutrient management equipment.
- AI plant recognition and growing management services.
- Agricultural solutions for schools, offices, and businesses.
- Hydroponic consumables, nutrient solutions, and replacement parts.

---

## 11. 开源计划 | Open Source Initiative

**中文**

项目计划逐步开放：

- PCB 原理图及设计文件。
- Gerber 和 BOM 文件。
- ESP32 固件及设备配置。
- Home Assistant 自动化配置。
- 后端及前端代码。
- AI 模型相关代码。
- 水培设施设计图纸。
- 安装、接线及维护文档。

各部分将根据其内容采用适合的开源许可证，并在 `LICENSES.md` 中明确说明。

**English**

The project plans to progressively release:

- PCB schematics and design files.
- Gerber and BOM files.
- ESP32 firmware and device configurations.
- Home Assistant automation configurations.
- Backend and frontend source code.
- AI-related source code.
- Hydroponic infrastructure design files.
- Installation, wiring, and maintenance documentation.

Appropriate open-source licenses will be assigned to individual project components and documented in `LICENSES.md`.

---

## 12. 项目愿景 | Vision

**中文**

OpenFarm AI 希望将智能家居、人工智能、自动化控制和现代农业结合起来，建立一套开放、模块化、可复制、可扩展的智能农业系统。

从家庭阳台到室内农场，从单套水培设备到企业级农业设施，让农业设备具备感知、分析、决策和自动执行能力。

**English**

OpenFarm AI aims to bring together smart home technology, artificial intelligence, automation, and modern agriculture to build an open, modular, reproducible, and scalable smart farming platform.

From home balconies to indoor farms, and from individual hydroponic units to enterprise agricultural facilities, our vision is to give agricultural systems the ability to sense, analyze, make decisions, and act autonomously.

---

**OpenFarm AI — Build Your Own Intelligent Farm.**

*Open Technology. Intelligent Agriculture. Sustainable Growing.*
