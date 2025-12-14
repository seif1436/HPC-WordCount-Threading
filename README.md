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
📊 Performance Metrics and ResultsThe following results were obtained using a dataset of approx. 30MB on an 8-core processor.MetricValueDescriptionSerial Time ($T_s$)0.1948 sBaseline execution time on a single core.Parallel Time ($T_p$)0.1259 sExecution time using 2 Threads.Speedup ($S$)1.55xRatio of $T_s / T_p$.Efficiency ($E$)77%Utilization of allocated resources.📈 Graphical Analysis(Refer to the Project Presentation for detailed charts and graphs).🧠 Discussion: Why is Speedup Limited?Despite using multi-threading, the speedup is not linear (i.e., 2 threads did not result in 2x speed). This is primarily due to:Python's GIL (Global Interpreter Lock): The GIL prevents multiple native threads from executing Python bytecodes at once. This means CPU-bound tasks (like counting words) essentially run in a serialized manner on the CPU, even if threaded.Context Switching Overhead: The cost of managing threads and switching context consumes a portion of the processing power.Ahmdal's Law: The theoretical speedup is always limited by the serial part of the program (reading the file and merging results).Conclusion: For CPU-intensive tasks in Python, multiprocessing is recommended over threading to bypass the GIL.🛠️ How to RunClone the Repository:Bashgit clone [https://github.com/seif1436/HPC-WordCount-Threading.git](https://github.com/seif1436/HPC-WordCount-Threading.git)
cd HPC-WordCount-Threading
Generate Dataset:Bashpython src/create_data.py
Run Benchmark:Open src/WordCount_Benchmark.ipynb in VS Code or Jupyter Notebook and run all cells.👥 Team MembersNameRoleSeif El-Din MohamedLead Developer & AnalysisMohamed EssamImplementation & TestingMohamed MedhatResearch & DocumentationSaeed Waled SaeedData Preparation & ValidationSupervised by: Dr. Hossam Reda Mohamed
