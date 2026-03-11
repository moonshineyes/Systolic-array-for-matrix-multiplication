# Systolic-array-for-matrix-multiplication
 Design a 4x4 INT8  Systolic Array Multiplier for matrix multiplication that minimizes dynamic power consumption during periods of data sparsity

# 4x4 Systolic Array Matrix Multiplier

A high-performance Verilog implementation of a 4x4 Systolic Array designed for INT8 matrix multiplication, optimized for ASIC/FPGA synthesis.

## 1. Overview
This project implements a data-flow driven systolic array where Processing Elements (PEs) pass data horizontally and vertically to compute $C = A \times B$.

## 2. Features
* **Wavefront Processing:** Synchronized data movement.
* **Low Power:** Optimized accumulation logic to skip zero-value multiplications using data sparsity optimization .
* **Clock Gating:** To make sure the gate is only used when necessary.

## 3. File Structure
* `pe.v`: The individual Processing Element logic.
* `systolic_array.v`: Top-level module connecting 16 PEs.
* `tb.v`: Testbench featuring Identity, Sparse, and Signed test cases.

