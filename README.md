# Matrix-Multiplication-Using-Multi-Threading

## Overview
This project evaluates the performance of multithreading in matrix multiplication by measuring execution time and CPU usage for different thread counts.

---

## Configuration
- Matrix Size: **1000 × 1000**
- Number of Matrices: **500**
- Language: **Python**
- Libraries: `numpy`, `matplotlib`, `psutil`, `concurrent.futures`

---

## Methodology
- Generated 500 random matrices and one constant matrix  
- Performed matrix multiplication using multiple threads  
- Varied thread count from **1 to 2 × CPU cores (20 threads)**  
- Measured execution time and CPU usage  
- Plotted performance graphs  

---

## Graphs

### Execution Time vs Threads
![Execution Time](graphs/time_vs_threads.png)

### CPU Usage vs Threads
![CPU Usage](graphs/cpu_vs_threads.png)

---

## Results & Insights

### ⏱ Execution Time
- Sharp decrease in time from **1 to ~5 threads**
- Minimum execution time achieved around **6–10 threads**
- After that, performance stabilizes with **no major improvement**
- Slight increase due to threading overhead beyond optimal point  

### CPU Usage
- CPU usage is **inconsistent** across threads  
- Peaks observed at certain thread counts (e.g., 3, 10, 15)  
- Overall utilization remains **moderate instead of maximum**  
- Indicates limitations due to:
  - Python GIL
  - System scheduling
  - Memory bottlenecks  

---

## Key Insight
- Best performance occurs **around optimal thread range (6–10 threads)**  
- Increasing threads beyond this does **not guarantee better performance**  
- Multithreading improves speed but has **diminishing returns**

---

## 🛠️ Installation
```bash
pip install numpy matplotlib psutil
