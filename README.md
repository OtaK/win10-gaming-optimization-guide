# Windows 10 Gaming Optimization Guide

Windows 10 version recommended: **2004**

## Introduction

The goal of this guide is to help people understand *why* and *how* to optimize their Windows systems for gaming.
Several areas of focus:

* DPC (*Deferred Procedure Call*) latency: Basically how fast your system responds to software state changes brought back by drivers.
* ISR (*Interrupt Service Routine*) latency: How fast your system processes hardware interrupts (= events).
* TCP/IP behavior: LOTS of unwanted behaviors for gaming are enabled by default in Windows, mainly because Windows is a general-purpose OS, so it's optimized for throughput and not latency.
* GPU drivers setup: Nvidia and AMD ship lots of bloat with their drivers by default, and they might cause latency in some cases.

## Measurement / Diagnostic Tools

* [LatencyMon](https://www.resplendence.com/latencymon): Allows you to check DPC and ISR latencies of your Windows system.
* [MouseTester](https://github.com/dobragab/MouseTester/releases/tag/v1.5.3): Allows you to check how well your mouse is polled. Mostly affected by the aforementioned DPC and ISR latencies.

## Tools

* [MSI Util v2](http://www.mediafire.com/file/2kkkvko7e75opce/MSI_util_v2.zip): Allows to toggle [MSI mode](https://forums.guru3d.com/threads/windows-line-based-vs-message-signaled-based-interrupts-msi-tool.378044/) and change interrupt priorities
* [TCP Optimizer](https://www.speedguide.net/downloads.php): All-in-one tool to fix TCP/IP behavior on Windows. It's possible to do it via `regedit` but much longer.
* The rest is already included in Windows :)

## Summary

* Part 1: Basic system setup
* Part 2: Taking care of drivers and devices
* Part 3: Optimizing your network
* Part 4: Getting rid of services you don't need
