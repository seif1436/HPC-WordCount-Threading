\# 🚀 Word Count Performance Analysis using Multi-threading



\## 📌 Project Overview

This project benchmarks the performance difference between \*\*Serial\*\* and \*\*Parallel\*\* execution for a CPU-bound task (Word Count) using Python. It explores the impact of Python's \*\*Global Interpreter Lock (GIL)\*\* on multi-threading performance.



This serves as \*\*Task 1\*\* for the High-Performance Computing (HPC) course.



\## 👥 Team Members

\* \*\*Seif El-Din Mohamed\*\*

\* Mohamed Essam

\* Mohamed Medhat

\* Saeed Waled Saeed



\*\*Supervised by:\*\* Dr. Hossam Reda Mohamed



\## ⚙️ Tech Stack

\* \*\*Language:\*\* Python 3.x

\* \*\*Libraries:\*\* `threading`, `multiprocessing`, `collections`, `time`, `os`

\* \*\*Tools:\*\* Jupyter Notebook, VS Code



\## 📊 Results \& Analysis

| Metric | Value |

|--------|-------|

| \*\*T\_serial\*\* | 0.1948 s |

| \*\*T\_p1\*\* | 0.1841 s |

| \*\*T\_pN (2 threads)\*\* | 0.1259 s |

| \*\*Speedup\*\* | \*\*1.55\*\* |

| \*\*Efficiency\*\* | \*\*0.77\*\* |



\### 💡 Key Observations:

1\. \*\*Speedup > 1:\*\* The parallel version achieved a speedup of \*\*1.55x\*\* using 2 threads, indicating better performance despite overhead.

2\. \*\*Efficiency (77%):\*\* Resource utilization is high, but slight overhead exists due to thread creation and merging.

3\. \*\*GIL Limitation:\*\* Python's GIL limits the true parallelism of CPU-bound tasks, preventing linear scalability with higher thread counts.



\## 📂 Project Structure

\* `src/create\_data.py`: Script to generate the dummy text dataset (approx 30MB).

\* `src/WordCount\_Benchmark.ipynb`: The main benchmarking logic (Serial vs Parallel).

\* `docs/Project\_Presentation.pdf`: Full presentation slides explaining the methodology and algorithms.



\## 🚀 How to Run

1\. Clone the repository.

2\. Run `create\_data.py` to generate the dataset.

3\. Open `WordCount\_Benchmark.ipynb` in VS Code or Jupyter.

4\. Run all cells to see the benchmark results.



---

\*Created by Seif El-Din Mohamed - 2025\*

