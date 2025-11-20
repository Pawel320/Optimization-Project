#  Microgrid Optimization – Numerical Optimization Project

This project implements several **LP-based optimization models** for a standalone microgrid including photovoltaic (PV) generation, battery storage, and optional wind power.  
All models are built using **JuMP** and solved with **Gurobi**, with performance comparison between the **Simplex** and **Barrier** algorithms.

---

##  Features

### **Task 2 – Base Microgrid Model**
- Cost minimization (PV + battery + grid usage)  
- Hourly SOC dynamics  
- Simplex / Barrier solver option  
- Exports LP files for sensitivity analysis  

### **Task 4 – Reduced SOC Model**
- SOC removed and replaced with cumulative energy constraints  
- Smaller LP, useful for benchmarking  

### **Task 3 – Solver Time Comparison**
- Benchmarks execution time for:
  - Simplex vs Barrier  
  - Full vs reduced model  
- Supports multi-year simulations  

### **Task 7 – CO₂ Minimization**
- Minimization of lifecycle CO₂ emissions  
- Includes PV, battery, and grid emission factors  
- Automatic search for sensitivity intervals  

### **Task 8 – Wind Power Scenarios**
- Multi-scenario robust LP (3 wind scenarios)  
- Shared PV/Battery/Wind investments  
- Minimizes worst-case + cumulative cost  

---


---

## 🛠 Requirements

Install these Julia packages:

```julia
using JuMP
using Gurobi
using Plots
using Statistics
using MathOptInterface
using Printf
using BenchmarkTools



This project was created for the Intro to Numerical Optimization course and demonstrates practical linear optimization applied to microgrid design.
