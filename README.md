# Catalan Spray and Wait Routing Protocol

## 📌 Overview
This project implements the **Catalan-based Spray and Wait (SnW) Routing Protocol** for **Delay Tolerant Networks (DTNs)**. It is an improved version of the **Binary SnW** protocol, optimized for **intermittently connected mobile networks**. 

🔹 **Key Highlights:**
- Implements **Spray and Wait** routing using the **Catalan number sequence**.
- Reduces the **wait phase**, improving delivery efficiency.
- Optimized for **real-world DTN simulations** (e.g., moving vehicles & pedestrians).
- Simulated using the **ONE Simulator**.

---

## 📂 Project Files
| File Name                  | Description |
|----------------------------|-------------|
| `catalan.java`             | Java implementation of **Catalan Spray and Wait** routing protocol. |
| `default_settings.txt`     | Configuration file for **ONE Simulator** (includes movement models, router settings, and message TTL). |
| `research paper catalan.pdf` | Research paper detailing the **Catalan-based routing method** and performance analysis. |

---

## ⚙️ How It Works
### 🏹 **Spray Phase**
✔️ Messages are **distributed using Catalan numbers** instead of binary division.  
✔️ If a message copy count `L` is **not a Catalan number**, the nearest **lower Catalan number** is used.  
✔️ The remaining copies are retained by the source node.  

### ⏳ **Wait Phase**
✔️ When a node has **only one copy left**, it **switches to direct transmission mode**.  
✔️ The message is **forwarded only when the destination is in range**.  

🔹 This **reduces redundant transmissions**, improving network efficiency.

---

## 🚀 Setup & Execution

### 🔧 **Prerequisites**
- **Java Development Kit (JDK)**
- **ONE Simulator** (Opportunistic Network Environment)

### 📌 **Steps to Run**
1. **Compile the Java Code**:
   ```sh
   javac catalan.java
