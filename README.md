
# OpenFarm AI

### 基于米家生态的企业级 AI 智能农业水培系统
### Enterprise AI-Powered Smart Hydroponics System Based on the Xiaomi Mi Home Ecosystem

<p align="center">

**让农业智能化，让种植自动化，让每个空间都成为智能农场。**

*Making Agriculture Intelligent, Growing Automated, and Every Space a Smart Farm.*

</p>

---

## 1. 项目简介 | Introduction

### 中文

OpenFarm AI 是一个面向家庭、企业、实验室、学校及商业农业场景的开源智能农业水培项目。

项目以小米米家生态（Xiaomi Mi Home）和 Home Assistant 为智能设备管理基础，结合自主研发的农业控制器、PCB 电路板、环境传感器、供水管路、营养液循环系统、加热设施及人工智能技术，构建一套模块化、自动化、可扩展的智能农业基础设施。

项目将智能家居、物联网、嵌入式硬件、自动化控制和 AI 技术应用于现代水培农业，实现对植物生长环境、水循环、温度、湿度、光照及营养液状态的统一监测与管理。

OpenFarm AI 不仅是一个水培设备，更是一个可扩展的智能农业平台。未来可应用于家庭种植、室内农场、育苗、实验室、学校、办公室及商业农业设施。

### English

OpenFarm AI is an open-source intelligent hydroponics project designed for residential, commercial, educational, laboratory, and agricultural applications.

Built around the Xiaomi Mi Home ecosystem and Home Assistant, the project combines custom agricultural controllers, PCB circuit designs, environmental sensors, water supply and circulation systems, nutrient management, heating infrastructure, and artificial intelligence technologies.

The platform integrates smart home technology, IoT, embedded hardware, automation, and AI to monitor and manage plant-growing environments, water circulation, temperature, humidity, lighting, and nutrient conditions.

OpenFarm AI is designed to be more than a hydroponic device. It aims to become a scalable intelligent agriculture platform for home growing, indoor farms, seedling cultivation, laboratories, schools, offices, and commercial agricultural facilities.

---

## 2. 项目愿景与目标 | Vision & Objectives

### 中文

项目希望建立一套开放、模块化、可复制、可扩展的智能农业系统。

主要目标：

- 建立基于米家生态的智能农业设备管理系统。
- 以 Home Assistant 为统一设备管理和自动化平台。
- 自主设计农业控制器、电路板及 PCB。
- 建立模块化水培种植架、供水、循环和排水系统。
- 实现温度、湿度、水位、水温、pH、EC 等参数监测。
- 集成水泵、电磁阀、补光灯、电热毯、加热器及通风设备。
- 建立农业设备自动化控制和远程监控能力。
- 逐步引入 AI 植物识别、生长分析及智能种植管理。
- 开放硬件设计、软件代码、设备接口及部署文档。

### English

The project aims to build an open, modular, reproducible, and scalable intelligent agriculture system.

Key objectives:

- Build an agricultural device management system based on the Xiaomi ecosystem.
- Use Home Assistant as the central device management and automation platform.
- Design custom agricultural controllers, circuit boards, and PCBs.
- Develop modular hydroponic growing structures, water supply, circulation, and drainage systems.
- Monitor temperature, humidity, water levels, water temperature, pH, and EC.
- Integrate pumps, solenoid valves, grow lights, heating mats, heaters, and ventilation equipment.
- Enable automated agricultural control and remote monitoring.
- Gradually introduce AI plant recognition, growth analysis, and intelligent cultivation management.
- Open-source hardware designs, software, device interfaces, and deployment documentation.

---

## 3. 第一阶段：项目可行性验证与基础原型

## Phase 1: Feasibility Study & Basic Prototype

<badge color="success">2026.11 — 2026.12</badge>

### 3.1 阶段定位 | Phase Definition

**中文**

第一阶段是 OpenFarm AI 项目的启动阶段，核心任务是验证整个项目的技术路线和工程可行性，并完成一套能够实际运行的基础智能水培原型。

本阶段不以建设完整的企业级农业系统为目标，而是优先完成最小可行产品（MVP），验证米家生态、Home Assistant、ESP32 控制器、传感器、供水系统和自动化设备之间能否实现稳定协同。

通过基础原型，验证项目在硬件设计、软件架构、农业设施和设备联动方面的可行性，为第二阶段的系统完善和功能扩展建立基础。

**English**

Phase 1 marks the initial development stage of OpenFarm AI.

The primary objective is to validate the technical approach and engineering feasibility of the project, while delivering a functional basic intelligent hydroponic prototype.

This phase does not aim to build a complete enterprise-scale agricultural system. Instead, it focuses on delivering a Minimum Viable Product (MVP) and validating the integration of Xiaomi Mi Home, Home Assistant, ESP32 controllers, sensors, water circulation systems, and automated equipment.

The prototype will demonstrate the feasibility of the hardware architecture, software platform, agricultural infrastructure, and device integration, establishing a foundation for future development.

### 3.2 第一阶段核心任务 | Core Tasks

**A. 基础农业设施 | Basic Agricultural Infrastructure**

- 搭建基础水培种植架。
- 安装储水箱及营养液容器。
- 完成基础供水、回水和排水管路。
- 安装循环水泵及供水设备。
- 建立基础水循环系统。
- 配置植物生长灯。
- 配置电热毯或育苗加热垫。
- 建立基本的通风和温度控制设施。

**B. 控制电路板与 PCB | Controller & PCB Development**

- 选择 ESP32 作为基础控制平台。
- 设计第一版农业控制器原理图。
- 完成基础 PCB Layout。
- 预留温湿度、水温、水位等传感器接口。
- 预留水泵、补光灯和其他执行器控制接口。
- 完成基础电源管理及接口保护设计。
- 制作或采购第一版 PCB。
- 完成基础固件烧录及功能测试。

**C. 传感器与数据采集 | Sensors & Data Acquisition**

第一阶段优先接入：

- 空气温湿度传感器。
- 水温传感器。
- 水位传感器。
- 光照传感器。
- 基础水泵运行状态检测。

在条件允许的情况下，开展 pH 和 EC 传感器的接入测试，为后续营养液自动管理做准备。

**D. 米家生态与智能联动 | Xiaomi Ecosystem Integration**

- 部署 Home Assistant。
- 接入支持的米家智能设备。
- 接入温湿度传感器或智能插座等设备。
- 实现 Home Assistant 对农业设备的统一监控。
- 建立基础自动化规则。
- 测试设备状态同步和远程控制。

**E. 基础自动化 | Basic Automation**

实现以下基础功能：

- 水泵定时启动和停止。
- 植物生长灯定时开关。
- 电热毯或育苗加热垫温度控制。
- 环境温湿度监测。
- 水箱液位监测。
- 设备异常状态提醒。
- 基础 Dashboard 数据展示。

### 3.3 第一阶段时间安排 | Phase 1 Timeline

| 时间 / Period | 研发任务 / Development Tasks | 预期成果 / Expected Results |
|---|---|---|
| 11月13日—11月20日 | 项目需求分析、技术选型、系统架构设计 | 完成技术方案和硬件清单 |
| Nov 13–20 | Requirements, technology selection, architecture design | Technical plan and hardware BOM |
| 11月21日—11月30日 | 水培结构搭建、传感器测试、控制板设计 | 基础设施和控制器初步完成 |
| Nov 21–30 | Hydroponic structure, sensor testing, controller design | Basic infrastructure and controller design |
| 12月1日—12月10日 | PCB 制作与测试、ESP32 固件开发、HA 部署 | 控制器初步运行，设备接入 HA |
| Dec 1–10 | PCB fabrication and testing, ESP32 firmware, HA deployment | Initial controller and HA integration |
| 12月11日—12月20日 | 水循环系统集成、米家设备联动、自动化调试 | 完成基础水培自动化 |
| Dec 11–20 | Water circulation integration, Xiaomi device integration, automation | Basic hydroponic automation |
| 12月21日—12月31日 | 原型联调、稳定性测试、文档整理及阶段验收 | 交付基础智能水培原型 |
| Dec 21–31 | Integration testing, stability validation, documentation, review | Basic intelligent hydroponic prototype |

### 3.4 第一阶段交付成果 | Phase 1 Deliverables

**中文**

截至 2026 年 12 月 31 日，计划完成以下成果：

1. 一套能够实际运行的基础水培原型。
2. 一套基础水培种植架及供水管路。
3. 一套 ESP32 农业控制器原型。
4. 第一版控制 PCB 设计文件或实物。
5. 基础环境传感器数据采集功能。
6. Home Assistant 运行环境。
7. 至少一种米家设备接入和联动演示。
8. 水泵、补光灯等基础设备自动化控制。
9. 温度及加热设备的基础控制演示。
10. 项目架构、接线、部署及测试文档。

**English**

By December 31, 2026, the planned deliverables include:

1. A functional basic hydroponic prototype.
2. A basic hydroponic growing rack and water pipeline system.
3. An ESP32-based agricultural controller prototype.
4. First-generation controller PCB design files or a physical prototype.
5. Basic environmental sensor data acquisition.
6. A working Home Assistant environment.
7. At least one demonstration of Xiaomi device integration and automation.
8. Basic automated control of pumps and grow lights.
9. Basic temperature monitoring and heating control demonstration.
10. Project architecture, wiring, deployment, and testing documentation.

### 3.5 第一阶段验收标准 | Phase 1 Acceptance Criteria

第一阶段以实际运行结果作为验收依据。

Phase 1 will be evaluated based on functional demonstrations and test results.

| 验收项目 / Criteria | 验收要求 / Acceptance Requirements |
|---|---|
| 水培设施 / Hydroponic Infrastructure | 能够完成基本供水、循环和排水 / Basic water supply, circulation, and drainage work |
| 控制器 / Controller | ESP32 能够正常运行并控制至少一种执行设备 / ESP32 operates and controls at least one actuator |
| 传感器 / Sensors | 至少两类环境或水培参数能够正常采集 / At least two types of environmental or hydroponic parameters are collected |
| Home Assistant | 能够正常显示设备状态和传感器数据 / Displays device states and sensor readings |
| 米家联动 / Xiaomi Integration | 至少一种支持的米家设备成功接入并演示联动 / At least one supported Xiaomi device is integrated and demonstrated |
| 自动化 / Automation | 至少完成水泵或补光设备的自动化控制 / At least one automated pump or lighting workflow works |
| 稳定性 / Stability | 完成连续运行测试并记录异常 / Complete a continuous operation test and document faults |
| 文档 / Documentation | 提供基础安装、接线和部署说明 / Provide basic installation, wiring, and deployment documentation |

### 3.6 第一阶段范围限制 | Phase 1 Scope Limitations

第一阶段暂不要求完成：

- 完整的 AI 植物病害识别系统。
- 自动配制及精准控制营养液。
- 大规模多区域农业管理。
- 完整商业级农业控制柜。
- 米家 App 原生硬件接入认证。
- 企业级云平台和多用户权限系统。
- 大规模商业化生产及认证。

这些内容将根据第一阶段的验证结果进入后续研发计划。

Phase 1 does not require a complete AI disease recognition system, automated nutrient formulation, large-scale multi-zone farm management, a fully commercial electrical control cabinet, native Mi Home hardware certification, an enterprise cloud platform, or commercial production certification.

These capabilities will be considered in subsequent development phases based on the results of the initial prototype.

---

## 4. 系统总体架构 | System Architecture

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
       Recommendations                |
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

## 5. 硬件系统 | Hardware Systems

### 5.1 主控电路板与 PCB 设计 | Controller & PCB Design

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

### 5.2 传感器系统 | Sensor Systems

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

### 5.3 水培与供水系统 | Hydroponics & Water Management

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

### 5.4 温度控制与加热设施 | Temperature Control & Heating

**中文**

计划支持：

- 电热毯及育苗加热垫。
- 水箱及营养液加热器。
- 根系区域加热设施。
- 温度传感器及温控模块。
- 保温棉及隔热材料。
- 环境通风及散热风扇。
- 自动温度控制与超温报警。

加热设备应符合当地电气规范，配置独立温控、过温保护及漏电保护。加热设备需与水源隔离。

**English**

Planned components:

- Electric heating blankets and seedling heat mats.
- Water tank and nutrient solution heaters.
- Root-zone heating systems.
- Temperature sensors and thermostat modules.
- Thermal insulation materials.
- Ventilation and cooling fans.
- Automatic temperature regulation and overtemperature alarms.

Heating equipment must comply with applicable electrical standards and include independent temperature control, overtemperature protection, and ground-fault protection. Heating equipment must be isolated from water sources.

### 5.5 光照与环境控制 | Lighting & Environmental Control

- LED 全光谱植物生长灯 / Full-spectrum LED grow lights.
- 自动补光控制 / Automated lighting control.
- 光照强度监测 / Light intensity monitoring.
- 自动通风系统 / Automated ventilation.
- 空气循环风扇 / Air circulation fans.
- 湿度控制设备 / Humidity control equipment.
- 温湿度联动控制 / Integrated temperature and humidity automation.

---

## 6. 软件与智能平台 | Software & Intelligence Platform

### Home Assistant

作为统一设备管理和自动化平台，接入米家设备及自主研发的农业硬件。

Serves as the central device management and automation platform, connecting Xiaomi devices and custom agricultural hardware.

### Xiaomi Mi Home Ecosystem

通过支持的米家设备和 Home Assistant 集成，实现温湿度监测、智能插座控制及其他设备联动。

Supported Xiaomi Mi Home devices can be integrated through Home Assistant for environmental monitoring, smart plug control, and device automation.

**说明 / Note:** 米家设备接入 Home Assistant，不等于自研硬件已经获得米家 App 原生接入能力。后续可根据小米 IoT 平台的接入条件探索原生生态集成。

Integrating Xiaomi devices with Home Assistant does not automatically make custom hardware natively compatible with the Mi Home app. Native integration may be explored subject to Xiaomi IoT platform requirements.

### ESP32 / ESPHome

用于农业控制器固件开发、传感器数据采集和执行器控制。

Used for agricultural controller firmware development, sensor data acquisition, and actuator control.

### MQTT

用于农业设备、Home Assistant 和 AI 平台之间的数据通信。

Provides messaging and data communication between agricultural devices, Home Assistant, and the AI platform.

### AI 智能系统 | AI Intelligence

计划开发：

- AI 植物生长状态识别 / AI plant growth recognition.
- 植物病害及异常识别 / Plant disease and anomaly detection.
- 生长周期记录与分析 / Growth cycle tracking and analysis.
- pH、EC 及环境数据分析 / pH, EC, and environmental data analysis.
- 智能补光和温度调节建议 / Intelligent lighting and temperature recommendations.
- 自动灌溉及营养液管理策略 / Automated irrigation and nutrient management.
- AI 种植助手及设备控制 Agent / AI growing assistant and equipment control agent.

AI 自动控制将结合设备权限、运行规则和安全阈值，避免模型直接执行不受约束的设备操作。

AI-driven automation will operate within defined permissions, operational rules, and safety thresholds.

---

## 7. 农业基础设施 | Agricultural Infrastructure

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

## 8. 安全设计 | Safety & Protection

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

Safety is a core design requirement because the system involves water, electricity, heating, and automated machinery.

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

## 9. 项目目录规划 | Repository Structure

```text
OpenFarm-AI/
│
├── README.md
├── LICENSES.md
│
├── hardware/
│   ├── controller/
│   │   ├── schematic/
│   │   ├── pcb/
│   │   ├── gerber/
│   │   └── bom/
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
│   ├── testing/
│   └── operation/
│
└── images/
    ├── prototype/
    ├── hardware/
    └── system-architecture/
```

---

## 10. 后续研发路线 | Future Development Roadmap

### 第二阶段：系统完善与农业自动化
### Phase 2: System Improvement & Agricultural Automation

**中文**

- 优化第一版农业控制器及 PCB。
- 扩展 pH、EC 和水质传感器。
- 实现更加完整的水循环及营养液监测。
- 优化自动灌溉和温度控制。
- 建立数据记录和历史趋势分析。
- 完善设备异常报警及远程监控。

**English**

- Improve the first-generation agricultural controller and PCB.
- Expand pH, EC, and water quality sensing.
- Develop more complete water circulation and nutrient monitoring.
- Improve automated irrigation and temperature control.
- Introduce data logging and historical trend analysis.
- Improve equipment alerts and remote monitoring.

### 第三阶段：AI 智能农业
### Phase 3: AI-Powered Agriculture

**中文**

- 建立植物图像采集系统。
- 开发 AI 植物识别及生长分析。
- 开发植物异常和病害识别能力。
- 开发 AI 种植助手。
- 探索基于传感器数据的种植策略优化。
- 实现受安全规则约束的 AI 自动控制。

**English**

- Build a plant image acquisition system.
- Develop AI plant recognition and growth analysis.
- Explore plant anomaly and disease detection.
- Develop an AI-powered growing assistant.
- Optimize cultivation strategies using sensor data.
- Implement AI automation under defined safety constraints.

### 第四阶段：企业级农业设施
### Phase 4: Enterprise Agricultural Infrastructure

**中文**

- 支持多种植区域管理。
- 支持多套水培设备集中控制。
- 建立统一农业设备管理平台。
- 建立数据记录、报表及告警系统。
- 支持远程运维和设备状态监控。
- 探索商业化农业设备及解决方案。

**English**

- Support multi-zone growing management.
- Enable centralized control of multiple hydroponic systems.
- Build a unified agricultural device management platform.
- Develop reporting, data logging, and alerting systems.
- Support remote maintenance and equipment monitoring.
- Explore commercial agricultural equipment and integrated solutions.

---

## 11. 商业化方向 | Commercial Opportunities

OpenFarm AI 采用开放平台与商业硬件相结合的模式。

OpenFarm AI combines an open technology platform with commercial hardware and services.

- 智能水培设备及种植系统 / Smart hydroponic equipment and growing systems.
- ESP32 农业控制器及 PCB 模块 / ESP32 agricultural controllers and PCB modules.
- pH、EC 和环境监测模块 / pH, EC, and environmental monitoring modules.
- 自动营养液管理设备 / Automated nutrient management equipment.
- AI 植物识别及种植管理服务 / AI plant recognition and growing management services.
- 学校、办公室及企业农业解决方案 / Agricultural solutions for schools, offices, and businesses.
- 水培耗材、营养液及替换配件 / Hydroponic consumables, nutrient solutions, and replacement parts.

---

## 12. 开源计划 | Open Source Initiative

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

## 13. 技术栈 | Technology Stack

| 技术 / Technology | 应用 / Application |
|---|---|
| Xiaomi Mi Home | 智能家居设备生态 / Smart home ecosystem |
| Home Assistant | 设备管理及自动化 / Device management and automation |
| ESP32 | 嵌入式控制器 / Embedded controller |
| ESPHome | 固件及设备集成 / Firmware and device integration |
| MQTT | 设备通信 / Device messaging |
| PCB Design | 控制电路板设计 / Controller circuit design |
| Python | 后端及数据处理 / Backend and data processing |
| FastAPI | API 服务 / API services |
| React | Web 管理界面 / Web management interface |
| OpenCV | 图像处理 / Image processing |
| AI Models | 植物识别及智能分析 / Plant recognition and intelligent analysis |
| Docker | 服务部署 / Service deployment |

---

## 14. 项目状态 | Project Status

<badge color="warning">Phase 1 — In Development / 第一阶段规划与研发中</badge>

| 项目模块 / Module | 当前状态 / Status |
|---|---|
| 项目架构 / Architecture | 规划中 / Planned |
| 水培基础设施 / Hydroponic Infrastructure | 规划中 / Planned |
| ESP32 控制器 / ESP32 Controller | 规划中 / Planned |
| PCB 设计 / PCB Design | 规划中 / Planned |
| 传感器系统 / Sensor System | 规划中 / Planned |
| Home Assistant | 计划部署 / Planned |
| 米家设备联动 / Xiaomi Integration | 待验证 / To Be Validated |
| 自动化控制 / Automation | 待开发 / To Be Developed |
| AI 植物识别 / AI Plant Recognition | 后续阶段 / Future Phase |
| 企业级管理平台 / Enterprise Platform | 后续阶段 / Future Phase |

项目状态将根据实际研发和测试结果持续更新。

Project status will be updated according to actual development and testing results.

---

## 15. 项目愿景 | Vision

**中文**

OpenFarm AI 希望将智能家居、人工智能、自动化控制和现代农业结合起来，建立一套开放、模块化、可复制、可扩展的智能农业系统。

第一阶段从基础水培原型开始，验证技术路线和工程可行性；未来逐步扩展至 AI 种植管理、多区域农业控制和企业级智能农业基础设施。

从家庭阳台到室内农场，从单套水培设备到企业级农业设施，让农业设备具备感知、分析、决策和自动执行能力。

**English**

OpenFarm AI aims to combine smart home technology, artificial intelligence, automation, and modern agriculture to build an open, modular, reproducible, and scalable intelligent farming platform.

Starting with a basic hydroponic prototype, the first phase will validate the technical architecture and engineering feasibility. Future development will expand toward AI-powered cultivation management, multi-zone agricultural control, and enterprise-scale smart farming infrastructure.

From home balconies to indoor farms, and from individual hydroponic units to enterprise agricultural facilities, our vision is to give agricultural systems the ability to sense, analyze, make decisions, and act autonomously.

---

## 16. 参与项目 | Contributing

欢迎开发者、硬件工程师、农业研究人员及开源社区成员参与项目。

Developers, hardware engineers, agricultural researchers, and open-source community members are welcome to contribute.

欢迎参与的方向 / Areas of contribution:

- PCB 及硬件设计 / PCB and hardware design.
- ESP32 固件开发 / ESP32 firmware development.
- Home Assistant 集成 / Home Assistant integration.
- 水培设施设计 / Hydroponic infrastructure design.
- AI 视觉识别 / AI visual recognition.
- 自动化控制 / Automation and control.
- 技术文档及测试 / Documentation and testing.

---

## 17. 许可证 | License

OpenFarm AI 计划采用分组件授权方式：

- 软件代码：AGPL-3.0。
- 硬件设计：CERN-OHL-S-2.0。
- 项目文档：CC BY-SA 4.0。

具体适用范围以各目录中的许可证文件和 `LICENSES.md` 为准。

OpenFarm AI plans to use component-specific licensing:

- Software: AGPL-3.0.
- Hardware designs: CERN-OHL-S-2.0.
- Documentation: CC BY-SA 4.0.

The applicable license for each component is defined by its corresponding license file and `LICENSES.md`.

---

<p align="center">

# OpenFarm AI

### Build Your Own Intelligent Farm.

**Open Technology · Intelligent Agriculture · Sustainable Growing**

</p>
