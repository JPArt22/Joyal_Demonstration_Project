# 🌳 Joyal Demonstration Lab

**Joyal Demonstration Lab** is an interactive computational environment designed to explore, visualize, and empirically validate **Joyal’s bijection** between functions  
\[
f : [n] \to [n]
\]
and the set of **labeled trees** on \( n \) vertices.

The project focuses on **real-time visual explanations**, **structured architecture**, and **immediate insight**, converting abstract combinatorics into an accessible laboratory experience.

---

## 📌 Philosophy

> **A fast, interactive laboratory where functions become trees.**  
> Priority: execution under **2 seconds**, with clear visuals and intuitive controls.

---

## 🧱 Architecture (5 Cells)

1. **Setup**  
   Silent installation of required libraries: `networkx`, `matplotlib`, `ipywidgets`.

2. **Classes**  
   - `FunctionGenerator`  
   - `JoyalBijection`  
   - `Visualizer`  
   All implemented cleanly inside one cell for modularity.

3. **Main Panel**  
   A graphical interface with **four synchronized visual panels**.

4. **Empirical Validation**  
   For all \( n \leq 5 \):  
   - generate all \( n^n \) functions  
   - convert each via Joyal  
   - verify that every tree appears exactly \( n^2 \) times  
   - confirm:  
     \[
     \frac{n^n}{n^2} = n^{n-2}
     \]

5. **Gallery**  
   Displays all \( n^{n-2} \) trees for \( n = 3, 4 \).  
   Clicking a tree reveals the \( n^2 \) functions that generate it.

---

## 🖥️ Main Panel (Cell 3)

### 🔧 Controls
- Slider for **n** (2 → 10), default **5**
- **Generate Random Function**
- **Run Full Bijection**
- **Verify Reversibility**

### 🖼️ Four-Panel Visualization

| Panel | Description |
|-------|-------------|
| **1** | Function graph \( f \) — **black arrows** |
| **2** | Decomposition — **red cycles**, **blue trees** |
| **3** | Joyal Tree — **purple root**, **green remaining nodes** |
| **4** | Verification — displays *“OK Confirmed”* |

---

## 🎨 Color Code

| Element | Color | Hex |
|---------|--------|------|
| Initial function | Black | `#000000` |
| Cycles | Red | `#FF3333` |
| Directed trees | Blue | `#3366FF` |
| Artificial root | Purple | `#9933FF` |
| Final tree | Green | `#00AA00` |

---

## 🔍 Empirical Validation (Cell 4)

For \( n \leq 5 \):

- enumerate all \( n^n \) functions  
- compute their Joyal tree  
- confirm that every labeled tree appears exactly \( n^2 \) times  

Result:  
\[
n^n / n^2 = n^{n-2} \quad \text{(confirmed)}
\]

---

## 🖼️ Gallery (Cell 5)

Displays all trees for:

- \( n = 3 \)  
- \( n = 4 \)

Selecting a tree reveals the complete set of generating functions.

---

## 🧪 Requirements

- Python 3.10+
- Jupyter / Google Colab
- Libraries:
  ```text
  networkx
  matplotlib
  ipywidgets
