# 李逍遥 · L-X-Yao

嵌入式软硬件工程师。飞控、工业控制、车载 ECU 三条线都从原理图做到批量交付，2022–2026 年在一家嵌入式产品公司主导 10 余个项目。

联系：lsc1476907630@gmail.com

## 开源

| 仓库 | 是什么 | 看点 |
|---|---|---|
| [ai-embedded-platform](https://github.com/L-X-Yao/ai-embedded-platform) | 259 个零依赖 C99 嵌入式组件加验证流水线 | 看点不是数量，是怎么检验 AI 写的固件代码：60 项审计、覆盖率门禁、fuzz、ARM 交叉编译；README 写明只有 5 个组件上过真机，查出的缺陷全部公开 |
| [argus](https://github.com/L-X-Yao/argus) | 浏览器端的 ArduPilot 地面站 | Svelte 5 + FastAPI，WebSerial 浏览器直连 USB，任务规划 / 标定 / RTK / 多机，10 种语言，3000+ 测试；ArduPilot 经 SITL 和真飞控台架验证，未做飞行测试 |
| [arduscope](https://github.com/L-X-Yao/arduscope) | ArduPilot .BIN 飞行日志诊断工具 | 把"飞得不好"翻译成"改哪个参数"：32 个分析器，每条判断注明出处（METHODIC 调参指南、ArduPilot wiki 或源码），参数建议可导出 .param；README 写明 20 条建议规则里 12 条在 SITL 里验证过，都没上过真机 |

## 做过的东西

| 项目 | 做了什么 | 结果 |
|---|---|---|
| 工业级飞控（垂起固定翼机型） | STM32H743 + STM32F103 IOMCU 双处理器、三层叠板、三余度异构 IMU、双气压计；ArduPilot/ChibiOS 板级定义（hwdef、bootloader）、USB 吞吐与 ESD 处理；外壳、三防漆、BOM、生产测试；适航配套文档 | 2025 年小批量交付 |
| 其他飞控 | 多旋翼和直升机的 ArduPilot 定制固件，出厂参数和使用指导；FPV 飞控硬件设计（STM32H743 主板加开关板） | 固件已发货多家客户 |
| PE 管热熔焊接机主控 | STM32H743，自研 4 层板；RT-Thread + 事件驱动分层状态机承载"装夹 → 铣削 → 加热 → 熔接 → 冷却"人机协同流程；自研 bootloader/OTA、错误码体系、SD 日志、现场操作卡 | 2023 年验收后量产，维护至 2026 年 |
| S32K344 车载 VCU 开发板 | NXP S32K344 + FS26 SBC，RTD 4.0 外设驱动，RT-Thread 移植，CAN / 车载以太网 / Bootloader；主讲配套的 S32K344 开发课程 | 整板成本核算、生产资料和测试流程，已小批量生产 |
| 五节三元锂 BMS | STM32F103 + BQ76920，RT-Thread nano；充放电与均衡、六类保护、SOC 估算与容量校准；检流电路 | 教学套件，2022 年首批约 200 套 |
| 其他 | 脊柱侧弯矫形器（ESP32，软硬件 + PCBA）、便携终端调试器（STM32F412 + CAN/DBC）、ESP32-BOX 桌面终端、802.11ah 数传（固件 + 载板）、GNSS 模块（NEO-M9N、UM982 RTK）、轮端检测（主从机 + LoRa）等 10 余项 | |
| 在校自学作品 | RT-Thread 多功能时钟、电子书阅读器、阿里云网关和子设备 | 2020–2021 年 |

## 怎么干活

- 软硬件一肩挑：原理图、多层 PCB、电源设计、RTOS 固件、上位机，一直做到量产导入，软硬件之间不用交接。
- 交付纪律：发布包按 git 哈希归档并附校验和，固件开机打印同一个哈希；现场问题以设备日志为准。
- 2026 年起用 AI 智能体开发：需求、验收标准、验证和现场调试我做，代码由 AI 按我定的规范写，过了门禁才能合入。上面三个仓库就是这么做出来的。

## 技能

ArduPilot（hwdef、ChibiOS 板级移植、QuadPlane）、MAVLink v2、NTRIP/RTK ｜ C/C99、RT-Thread、ChibiOS、FreeRTOS、分层状态机、Bootloader/OTA、CAN / LIN ｜ STM32 F1/F4/H7、GD32、ESP32、S32K344、PY32 ｜ 原理图、4 层及以上 PCB、电源树、模拟前端、Altium / 立创专业版 ｜ Python、TypeScript / Svelte 5、GitHub Actions

---

Embedded hardware/firmware engineer: industrial flight controllers (ArduPilot, STM32H7), industrial machine control (RT-Thread), vehicle control unit dev boards (S32K344). Since 2026 I build with AI agents under contracts and gates I define; the three repositories above are the result.
