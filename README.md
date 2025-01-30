# Catalan Spray and Wait Routing Protocol

## Overview
This project implements a **Catalan-based Spray and Wait Routing Protocol** for **Delay Tolerant Networks (DTN)**, inspired by the paper **"An Improved Delay Tolerant Routing Protocol for Opportunistic Networks"**.

Unlike traditional **Binary Spray and Wait**, this approach distributes message copies based on **Catalan numbers**, improving delivery efficiency and reducing overhead.

## Features
- Implements **Spray and Wait** routing with a **Catalan-based message copy distribution**.
- Reduces the wait phase compared to **Binary SnW**, improving message delivery.
- Simulated using the **ONE Simulator**.
- Optimized for **intermittently connected mobile networks**.

## Files
- `catalan.java`: Java implementation of the **Catalan Spray and Wait routing algorithm**.
- `default_settings.txt`: Configuration file for simulation settings.
- `research paper catalan.pdf`: Research paper explaining the **Catalan-based routing method** and performance analysis.

## How It Works
1. **Spray Phase**:
   - Messages are distributed based on the **Catalan sequence** rather than binary division.
   - If a message copy count `L` is not a Catalan number, the nearest lower **Catalan number** is used.
   - Remaining copies are kept by the source node.

2. **Wait Phase**:
   - Once a node has **one copy left**, it switches to **direct transmission mode**.
   - The message is forwarded **only when the destination is in range**.

## Setup and Execution
### **Prerequisites**
- Java Development Kit (JDK)
- ONE Simulator (Opportunistic Network Environment)

### **Steps to Run**
1. **Compile the Java Code**:
   ```sh
   javac catalan.java
