<div align="center">

 This is a community-curated hub for open-source operating systems, standards, and resources for satellite onboard computers and payloads, maintained by the **[OPENSAT](https://github.com/Satellite-OSS)** open-source satellite community.

[![Discussions](https://img.shields.io/badge/Discussions-Join%20the%20Community-2ea44f?style=flat-square&logo=github)](https://github.com/orgs/Satellite-OSS-BUPT/discussions)
[![README](https://img.shields.io/badge/README-中文-blue?style=flat-square)](README.zh-CN.md)

**English** | [中文](README.zh-CN.md)

</div>

---

## 📂 Available Resources: (`docs/`)

Currently this repository shares documents in the `docs/` directory, which collects industry standards, specifications, whitepapers and reports related to satellite operating systems, so that the community has a common place to find the material that guides design, implementation, evaluation and collaboration.

| Document | Description |
| --- | --- |
| [Open Standard Initiative for Space Operating Systems (太空操作系统开源标准倡议)](docs/太空操作系统开源标准倡议-修改.pdf) | The community's initiative document on open standards for space operating systems. |

More material is welcome here, for example: space system standards and recommendations (e.g., CCSDS, ECSS), POSIX profiles and RTOS interface specifications, safety, security and qualification/certification guidance, and whitepapers or technical reports from industry, academia and open-source projects. If you would like to add a document, simply open a pull request with the file placed under `docs/`.

---

## 📡 Popular Open-Source Satellite Operating Systems

The projects below are grouped into three categories: operating systems optimized specifically for satellite scenarios; general-purpose open-source real-time operating systems (RTOSes) suitable for satellite scenarios; and operating systems for COTS devices (such as Raspberry Pi-class single-board computers) used as satellite payloads.

### 1️⃣ Open-Source OSes Optimized for Satellite Scenarios

- **[RROS](https://github.com/BUPT-OS/RROS)** — A dual-kernel open-source operating system developed by BUPT-OS, composed of a real-time kernel implemented in Rust and a general-purpose Linux kernel. It is designed primarily for satellites whose onboard computers and payloads must run both traditional satellite-borne real-time tasks (e.g., communication and positioning) and complex general-purpose tasks (e.g., data compression and machine learning). RROS is compatible with almost all native Linux programs, offers hard real-time performance superior to RT-Linux, and exposes its real-time APIs to user programs through the libevl interface, with debugging supported by tools such as gdb, kgdb and QEMU. It was open-sourced in November 2023, was successfully launched into space in December 2023, and is being experimented with as the host OS for in-orbit satellites ([Tiansuan Project](http://www.tiansuan.org.cn/)). Its documentation and quick-start guides are available on the [project website](https://bupt-os.github.io/website/docs/).

### 2️⃣ General-Purpose Open-Source RTOSes Suitable for Satellite Scenarios

The following are two representative general-purpose open-source RTOSes that are suitable for satellite scenarios:
- **[Apache NuttX](https://github.com/apache/nuttx)** — An Apache Software Foundation real-time operating system that emphasizes standards compliance and a small footprint, scalable from 8-bit to 64-bit microcontroller environments. Because it is small, highly portable across a wide range of architectures and boards, POSIX-compliant and licensed under Apache-2.0, it is a practical foundation for onboard payload controllers, instruments and other satellite software that cannot afford a large OS footprint.

- **[RTEMS](https://github.com/RTEMS/rtems)** — The Real-Time Executive for Multiprocessing Systems, an open-source real-time executive (kernel) with a long heritage in aerospace and defense. Its link-time configurability and mature engineering make it a well-established choice for long-lived onboard flight software. Note that this GitHub repository is a mirror — development happens at [gitlab.rtems.org](https://gitlab.rtems.org/rtems/rtos/rtems), with documentation at [docs.rtems.org](https://docs.rtems.org/).

### 3️⃣ General-Purpose OSes for COTS Devices

The third category is a relatively cutting-edge one. Commercial off-the-shelf (COTS) embedded devices have gradually become an important part of satellite payloads, and the general-purpose operating systems running on them can also be carried onboard. **Linux distributions**(e.g., Debian, Fedora) are the typical example: the same kernel, drivers and user-space stack that run on a developer's desk can be deployed on a payload processor, so teams can reuse mature file systems, networking, containerization, language runtimes and AI frameworks, and can iterate quickly between ground hardware and flight hardware.

---

## 🤝 Contributing

Researchers, developers, students and satellite enthusiasts are all welcome. 
👉 **[Join the Discussions](https://github.com/orgs/Satellite-OSS-BUPT/discussions)**

