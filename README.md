# Matrix-Multiplication-Using-Multi-Threading

## Overview
This project evaluates the performance of multithreading in matrix multiplication by measuring execution time and CPU usage for different thread counts.

---

## 🧠 What is Multithreading?
Multithreading is a technique where multiple threads (smaller units of a process) run concurrently within a program. It allows tasks to be divided and executed in parallel, improving performance for computationally intensive operations.

### Why use it here?
Matrix multiplication is a CPU-intensive task. By distributing multiple matrix multiplications across threads, we can:
- Reduce execution time  
- Utilize CPU resources more efficiently  
- Process multiple operations simultaneously

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
<img width="584" height="455" alt="Execution Time vs Threads" src="https://github.com/user-attachments/assets/cadc0d46-d486-4bc4-b8e9-c9d8d1986cc2" />


### CPU Usage vs Threads
<img width="562" height="455" alt="CPU Usage vs Threads" src="https://github.com/user-attachments/assets/4e1ba9e6-7c9f-4947-8026-bf63fb860a46" />


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

## Key Insights
- Best performance occurs **around optimal thread range (6–10 threads)**  
- Increasing threads beyond this does **not guarantee better performance**  
- Multithreading improves speed but has **diminishing returns**

---
