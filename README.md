# 🚀 High-Performance Computing: Word Count Analysis

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Threading](https://img.shields.io/badge/Concurrency-Multi--Threading-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Course](https://img.shields.io/badge/Course-HPC-blueviolet?style=for-the-badge)

> **A benchmarking study comparing Serial vs. Parallel execution for CPU-bound tasks in Python, analyzing the impact of the Global Interpreter Lock (GIL).**

---

## 📖 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Project Architecture](#-project-architecture)
- [Performance Metrics](#-performance-metrics-and-results)
- [Discussion (The GIL Problem)](#-discussion-why-is-speedup-limited)
- [Team Members](#-team-members)

---

## 📌 Project Overview
This project implements a **Word Count** algorithm using two different approaches to measure performance scaling:
1.  **Serial Execution:** Single-threaded processing.
2.  **Parallel Execution:** Multi-threaded processing using Python's `threading` module with data chunking.

The main objective is to analyze the trade-off between **parallelism overhead** and **execution speed** in a Python environment.

---

## 🌟 Key Features
* **Data Generation:** Automated script to generate large-scale dummy text datasets (30MB+).
* **Smart Chunking:** Algorithms to split data evenly across available threads.
* **Benchmarking Engine:** Precise time measurement for Serial vs. Parallel execution.
* **Metric Calculation:** Automatic computation of Speedup, Efficiency, and Scalability.

---

## 📂 Project Architecture

```text
HPC-WordCount-Threading/
├── src/
│   ├── WordCount_Benchmark.ipynb   # Main Logic & Analysis (Jupyter)
│   └── create_data.py              # Dataset Generator Script
├── docs/
│   └── Project_Presentation.pdf    # Detailed Scientific Report
├── data/
│   └── wordcount_sample_2MB.txt    # Generated Dataset (excluded from repo)
└── README.md                       # Documentation
