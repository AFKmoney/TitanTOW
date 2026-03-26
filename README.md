<div align="center">

# TitanTOW

### Ternary-Over-Windows Performance Engine

**Transform your CPU into a bare-metal compute machine. Overpower your Silicon.**

[![License](https://img.shields.io/badge/License-DAEMONLab_Proprietary-black?style=flat-square)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows_10%2F11-blue?style=flat-square)]()
[![Build](https://img.shields.io/badge/Built_With-Rust-orange?style=flat-square)]()
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)]()

</div>

---

## 🛑 The Problem

Every standard Windows PC is fighting itself.

Your game engine, your browser, your antivirus, and the OS all share the same CPU cores — context-switching every few milliseconds, evicting each other from cache, injecting micro-stutters that compound into real-world latency.

The kernel doesn't know your priorities. It treats everything equally.

**TitanTOW fixes this.** TITAN is not a generic "PC Booster" that just closes programs you don't need. It is a **Bare-Metal Hardware Optimizer** that bypasses the Windows thread scheduler by overriding the OS affinity masks.

---

## 🚀 The T.O.W. Architecture

Through its proprietary **Ternary-Over-Windows (T.O.W.)** architecture, TitanTOW physically isolates your CPU cores into three strict tiers:

```
[ TIER +1 : POSITIVE ] → Exclusive Cores reserved strictly for Heavy Compute 
[ TIER  0 : UNKNOWN  ] → Neutral Cores where Windows and necessary background services are confined
[ TIER -1 : NEGATIVE ] → Starvation Cores where parasitic processes (telemetry, bloated apps) are throttled
```

It seizes control of the silicon to eliminate the cache pollution that kills frame times and render performance. No polling. No user input. Autonomous and continuous.

### Supported "TIER +1" Applications
TITAN automatically detects and elevates the following applications out of the box. No configuration required:
- **Gaming:** CS2, DOTA 2, Cyberpunk 2077, Elden Ring, Valorant, Fortnite, GTA V, etc.
- **Creative:** Premiere, DaVinci Resolve, Photoshop, Blender, Unreal Engine, Unity.
- **Dev/Compute:** Visual Studio, Rustc, Python, Node, Hashcat.

---

## ⚡ Measured Results

Benchmarked on **AMD Ryzen 7 5800H** (Beelink SER5):

| Metric | Before TitanTOW | After TitanTOW |
|:-------|:---------------:|:--------------:|
| L1 Cache Latency | 1.24 ns | **0.95 ns** |
| Memory Throughput | 16.4 GB/s | **19.9 GB/s** |
| CPU Clock Detected | 2.13 GHz | **2.92 GHz** |
| OS Jitter | 510 µs | **379 µs** |

> All measurements are cycle-accurate, taken directly from the CPU's Time Stamp Counter (RDTSC). Not Windows Performance APIs.

---

## 🛠️ Installation & Usage

TitanTOW is designed for professionals and enthusiasts who demand zero-latency computing. It installs as a background Windows Service and runs 24/7.

1. Download **`TITAN_Installer_v2.exe`** from the [latest release](../../releases/latest)
2. Right-click → **Run as Administrator**
3. Follow the installer wizard

*(To uninstall: Run TITAN from the command line with `--uninstall`)*

### Silicon Verification (Benchmark)

To verify that TITAN has successfully seized control of your hardware caches:

Open PowerShell as Administrator, navigate to the install directory, and run the benchmark:
```powershell
cd "C:\Program Files\DAEMONLab\TITAN\"
.\titan.exe --bench
```
This bypasses standard OS metrics and reads directly from the CPU's RDTSC to show your raw L1 Cache latency, Memory bandwidth, and OS Jitter reduction.

---

## ❓ FAQ

**Q: Why does my CPU usage in Task Manager look different?**
**A:** TITAN breaks standard OS telemetry. By pinning threads to specific physical cores and bypassing the Windows scheduler, the native Task Manager often misreports thread activity. Use TITAN's `--bench` flag for true measurements.

**Q: Do I need to reboot?**
**A:** No. TITAN seizes control dynamically at runtime.

---

## 💻 Compatibility & Tech Stack

| | |
|:---|:---|
| **OS** | Windows 10 / 11 (64-bit) |
| **CPU** | x86-64 with AVX2 + BMI2 + POPCNT |
| **Dependencies** | Zero — no .NET, no Python, no runtimes |

Built from scratch in **Rust**. Zero third-party dependencies in the hot path. Compiled with maximum optimization flags.

> **Legal:** The source code is closed and proprietary. Reverse engineering is prohibited under the DAEMONLab License.

---

<div align="center">

*DAEMONLab XN.CORE &copy; 2026 &mdash; All rights reserved.*

</div>
