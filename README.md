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

### ⚖️ **Prerequisites**
- **Java Development Kit (JDK)**
- **ONE Simulator** (Opportunistic Network Environment)

### 📈 **Steps to Run**
1. **Compile the Java Code**:
   ```sh
   javac catalan.java
   ```
2. **Run the Simulation**:
   - Configure **`default_settings.txt`** as required.
   - Run the **ONE Simulator** to observe **Catalan routing behavior**.

---

## 📊 Performance Evaluation
### **Evaluation Metrics**
📌 **Delivery Ratio** - Measures the percentage of successfully delivered messages.  
📌 **Overhead Ratio** - Represents redundant message copies compared to delivered messages.  
📌 **Mean Delay** - Average time taken for message delivery.  
📌 **Average Hop Count** - Number of intermediate nodes the message passes through.  

### **Performance Comparison**
| Number of Copies | Wait Phase Level (Binary SnW) | Wait Phase Level (Catalan SnW) |
|-----------------|-----------------------------|-----------------------------|
| **6**  | 2 | **1** |
| **8**  | 3 | **2** |
| **10** | 3 | **3** |
| **12** | 3 | **3** |
| **14** | 3 | **3** |
| **16** | 4 | **2** |
| **32** | 5 | **4** |

🔹 **Catalan SnW outperforms Binary SnW** by reaching the wait phase **faster**, reducing overhead, and improving efficiency.

---

## 📚 References
- **Mushtaq Ahmed, Amit Yadav** - "An Improved Delay Tolerant Routing Protocol for Opportunistic Networks".
- Research on **Spray and Wait Routing Protocols** in DTNs.

---

## 📝 License
This project follows the **GPLv3 License** as stated in the source code.

---

## 🤝 Contributing
Want to improve the routing algorithm or enhance the simulation?  
📩 Feel free to open **issues** or submit **pull requests**!  

---

💡 **Happy Coding! 🚀**

