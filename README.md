# 李逍遥（李思成）· L-X-Yao

嵌入式软硬件全栈工程师。飞控、工业控制、车载 ECU 三条线都从原理图做到量产交付，2022 年起在一家嵌入式产品公司主导 10 余个项目。

## 做过的东西

| 项目 | 做了什么 | 结果 |
|---|---|---|
| ISTD-100 工业级飞控（垂起固定翼机型） | STM32H743 + STM32F103 IOMCU 双处理器、三层叠板、三余度异构 IMU、双气压计；ArduPilot/ChibiOS 板级定义（hwdef、bootloader）、USB 吞吐与 ESD 处理；外壳、三防漆、BOM、生产测试；适航配套文档 | 2025 年量产交付 |
| PE 管热熔 / 电熔焊接机主控 | 对标 Gator 的正向复刻：STM32H7 + ESP32，自研 4 层板，重构模拟供电（纹波 <10 mV）；RT-Thread + 事件驱动分层状态机承载"装夹 → 铣削 → 加热 → 熔接 → 冷却"人机协同流程；自研 bootloader/OTA、错误码体系、SD 日志、现场操作卡 | 热熔机 2023 年验收，电熔机 2025 年验收，持续维护至 2026 年 |
| 车载 VCU 平台 | NXP S32K344 + FS26 SBC，RTD 4.0 外设驱动，RT-Thread 移植，CAN / 车载以太网 / Bootloader | 整板成本核算、生产资料和测试流程，已量产 |
| 五节三元锂 BMS | STM32F103 + BQ76920，RT-Thread nano；充放电与均衡、六类保护、SOC 估算与容量校准；检流电路 | 可用样机 |
| 其他 | 脊柱侧弯矫形器（ESP32，软硬件 + PCBA）、便携终端调试器（STM32F412 + CAN/DBC）、国产兼容三菱 FX3U PLC、ESP32-BOX 桌面终端、802.11ah 数传固件等 10 余项 | |

## 开源

| 仓库 | 是什么 | 看点 |
|---|---|---|
| [ai-embedded-platform](https://github.com/L-X-Yao/ai-embedded-platform) | 259 个零依赖 C99 嵌入式组件加验证流水线 | 看点不是数量，是怎么让 AI 生成的固件代码值得信任：63 项审计、覆盖率门禁、fuzz、ARM 交叉编译；README 写明了哪些上过真机、哪些没有 |
| [argus](https://github.com/L-X-Yao/argus) | 浏览器里即开即用的 MAVLink 地面站 | Svelte 5 + FastAPI + Tauri v2，WebSerial 浏览器直连 USB，任务规划 / 标定 / RTK / 多机，10 种语言，1800+ 测试，ArduPilot 实机验证 |

## 怎么干活

- 软硬件一肩挑：原理图、多层 PCB、电源完整性、RTOS 固件、上位机到量产导入，不在软硬件之间做交接。
- 交付纪律：发布包按 git 哈希归档并附校验和，开机横幅带版本，现场日志是判读设备行为的唯一依据。
- 2026 年起用 AI 智能体做整块开发：需求、验收标准、验证和现场调试我做，代码由 AI 在我定的合约和门禁下写。上面两个仓库就是这么做出来的。

## 技能

ArduPilot（hwdef、ChibiOS 板级移植、QuadPlane）、MAVLink v2、NTRIP/RTK ｜ C/C99、RT-Thread、ChibiOS、FreeRTOS、分层状态机、Bootloader/OTA ｜ STM32 F1/F4/H7、GD32、ESP32、S32K344、PY32、飞腾派 E2000 ｜ 原理图、4 层及以上 PCB、电源树、模拟前端、Altium / 立创专业版 ｜ Python、TypeScript / Svelte 5、Tauri v2、GitHub Actions

---

Embedded hardware/firmware engineer: industrial flight controllers (ArduPilot, STM32H7), industrial machine control (RT-Thread), vehicle control units (S32K344). Since 2026 I build with AI agents under contracts and gates I define; the two repositories above are the result.
