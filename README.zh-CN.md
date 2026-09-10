<div align="center">

这是一个由 **[OPENSAT](https://github.com/Satellite-OSS)** 卫星开源社区维护，汇聚面向卫星星载计算机与载荷的开源操作系统、标准与其他相关资源的开源仓库。

[![Discussions](https://img.shields.io/badge/Discussions-Join%20the%20Community-2ea44f?style=flat-square&logo=github)](https://github.com/orgs/Satellite-OSS-BUPT/discussions)
[![README](https://img.shields.io/badge/README-English-blue?style=flat-square)](README.md)

[English](README.md) | **中文**

</div>

---
## 📂 已收录资源：（`docs/`）

目前本仓库的文档统一放在 `docs/` 目录中。该目录用于分享与卫星操作系统相关的行业标准、规范、白皮书和研究报告，为社区提供一个集中查找设计、实现、评估与协作依据的地方。

| 文档 | 简介 |
| --- | --- |
| [太空操作系统开源标准倡议](docs/太空操作系统开源标准倡议-.pdf) | 社区关于太空操作系统开放标准的倡议文档。 |

我们也欢迎更多资料加入这里，例如：航天系统标准与建议（如 CCSDS、ECSS）、POSIX 规范与实时操作系统接口规范、安全与鉴定/认证指南，以及来自产业界、学术界和开源项目的白皮书或技术报告。如果你想补充文档，只需将文件放入 `docs/` 后提交 Pull Request。

---

## 📡 受欢迎的开源卫星操作系统

下面把相关开源项目分为三类：专为卫星场景优化的操作系统；适用于卫星场景的通用开源实时操作系统；适用于卫星载荷的COTS设备（如树莓派级别的单板计算机）的操作系统。

### 1️⃣ 专为卫星场景优化的开源 OS

- **[RROS](https://github.com/BUPT-OS/RROS)** —— 由 BUPT-OS 开发的「双内核」开源操作系统，由一个用 Rust 实现的实时内核和一个通用的 Linux 内核组成。它主要面向这样一类卫星：星载计算机与载荷既需要运行传统的星上实时任务（如通信、定位），又需要运行复杂的通用任务（如数据压缩、机器学习）。RROS 兼容几乎所有的原生 Linux 程序，实时性能优于 RT-Linux，并通过 libevl 接口向用户态程序提供实时 API，支持 gdb、kgdb、QEMU 等工具进行调试。该项目于 2023 年 11 月开源，2023 年 12 月成功发射入轨，目前正作为在轨卫星的宿主操作系统开展试验（[天算计划](http://www.tiansuan.org.cn/)）。文档与快速上手指南见[项目网站](https://bupt-os.github.io/website/docs/)。

### 2️⃣ 适用于卫星场景的通用开源 RTOS

- **[Apache NuttX](https://github.com/apache/nuttx)** —— 由 Apache 软件基金会维护的实时操作系统，强调标准合规与小体积，可从 8 位扩展到 64 位微控制器环境。它主要遵循 POSIX 和 ANSI 标准，并对标准未覆盖的功能补充了 Unix 以及其他常见实时操作系统（如 VxWorks）风格的 API。由于体积小、可移植性强（支持大量架构与开发板）、符合 POSIX 且采用 Apache-2.0 许可，它是星载载荷控制器、仪器等无法承受庞大 OS 体积的卫星软件的实用基础。

- **[RTEMS](https://github.com/RTEMS/rtems)** —— 全称 Real-Time Executive for Multiprocessing Systems，是一款开源实时内核，在航空航天与国防领域有着悠久的历史传承。它提供基于标准的接口（POSIX 1003.1 API 以及自身的 Classic API）、多任务、事件驱动且基于优先级抢占的调度（可选单调速率调度）、优先级继承、支持 EDF 集群调度的对称多处理（SMP）、通过运行时链接实现的动态代码加载，以及 IMFS、FAT、RFS、JFFS、NFSv4（借助 LibBSD）等文件系统，并提供 I2C、SPI、USB、SD/MMC 与帧缓冲设备驱动。其链接期可配置能力与成熟的工程化实践，使其成为长寿命星载飞行软件的经典选择。注意：该 GitHub 仓库仅为镜像，实际开发在 [gitlab.rtems.org](https://gitlab.rtems.org/rtems/rtos/rtems)，文档见 [docs.rtems.org](https://docs.rtems.org/)。

### 3️⃣ COTS设备的通用 OS

第三类是比较前沿的一类。商用现货（COTS）嵌入式设备已日渐成为卫星载荷的重要组成部分，其上运行的各类通用操作系统也能被搭载到卫星上。**Linux 各类发行版**（例如Debian，Fedora）就是典型代表：卫星能够运行在开发者桌面上的同一套内核、驱动与用户态软件栈，可以直接部署到载荷处理器上，团队因此能够复用成熟的文件系统、网络、容器化、语言运行时和 AI 框架，并在地面硬件与卫星硬件之间快速迭代。

---

## 🤝 贡献倡议

欢迎研究人员、开发者、学生和卫星爱好者参与贡献。

👉 **[加入讨论区](https://github.com/orgs/Satellite-OSS-BUPT/discussions)**

