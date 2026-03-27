# 🚀 Python Advance Complete Tutorial - Part 4 🐍🔍

![GitHub Repo stars](https://img.shields.io/github/stars/your-username/Python_Advance_Complete_Tutorial_Part_4?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/your-username/Python_Advance_Complete_Tutorial_Part_4?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/your-username/Python_Advance_Complete_Tutorial_Part_4?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge&logo=python)

---

# 📚 Table of Contents 📌
- 📖 Introduction
- 📂 Repository Structure
- 📁 Folder Details
- 📜 Notebook Descriptions
- 🔍 Linear Search — Recursive Flowchart
- 🔎 Binary Search — Recursive Flowchart
- ⚡ Complexity Comparison
- ⚙️ How to Use
- 🌟 Key Highlights
- 🤝 Contributing
- 📬 Contact

---

# 📖 Introduction ✨

This repository is **Part 4** of the Python Advance Complete Tutorial series.

It covers **Searching Algorithms** implemented entirely through **Recursion** — reinforcing both algorithmic thinking and recursive problem solving simultaneously.

You will learn:
- How to recursively scan every element to find a target (Linear Search)
- How to recursively halve the search space to find a target (Binary Search)

---

# 📂 Repository Structure 🗂️

```
Python_Advance_Complete_Tutorial_Part_4/
└── Searching Algorithms in Python/
    ├── Python Linear Search.ipynb
    └── Python Binary Search.ipynb
```

---

# 📁 Folder Details 📂

📌 **Searching Algorithms in Python**

---

# 📜 Notebook Descriptions 📘

| Notebook | Algorithm | Approach | Time Complexity | Requires Sorted Array |
|---|---|---|---|---|
| Python Linear Search.ipynb | Linear Search | Recursive | O(n) | No |
| Python Binary Search.ipynb | Binary Search | Recursive | O(log n) | Yes |

---

# 🔍 Linear Search — Recursive Flowchart 📊

Linear Search scans each element one by one using recursive calls. At each call, it checks two base cases: (1) index out of bounds → return -1, (2) element matches target → return index. Otherwise it recurses with `i + 1`.

```mermaid
graph TD
    A["linear_search(arr, target, i)"] --> B{i >= len arr?}
    B -- Yes --> C[return -1]
    B -- No --> D{arr[i] == target?}
    D -- Yes --> E[return i]
    D -- No --> F["recurse: linear_search(arr, target, i+1)"]
    F --> A
```

> **Initial call:** `linear_search(arr, target, 0)`

---

# 🔎 Binary Search — Recursive Flowchart 📊

Binary Search eliminates half the search space at each recursive call. It requires a sorted array. At each call: compute `mid`, check base cases, then recurse either left (`hi = mid - 1`) or right (`lo = mid + 1`).

```mermaid
graph TD
    A["binary_search(arr, target, lo, hi)"] --> M["mid = (lo + hi) // 2"]
    M --> B{lo > hi?}
    B -- Yes --> C[return -1]
    B -- No --> D{arr[mid] == target?}
    D -- Yes --> E[return mid]
    D -- No --> F{arr[mid] < target?}
    F -- Yes --> G["recurse: lo = mid + 1"]
    F -- No --> H["recurse: hi = mid - 1"]
    G --> A
    H --> A
```

> **Initial call:** `binary_search(arr, target, 0, len(arr) - 1)`

---

# ⚡ Complexity Comparison 📈

| Property | Linear Search | Binary Search |
|---|---|---|
| Time Complexity | O(n) | O(log n) |
| Space Complexity (recursive) | O(n) | O(log n) |
| Works on unsorted array | Yes | No |
| Implementation | Recursive | Recursive |
| Best case | O(1) | O(1) |
| Worst case | O(n) | O(log n) |

---

# ⚙️ How to Use 🛠️

1. Clone the repository 📥
```bash
git clone https://github.com/your-username/Python_Advance_Complete_Tutorial_Part_4.git
cd "Searching Algorithms in Python"
```

2. Open Jupyter Notebook 📓
```bash
jupyter notebook
```

3. Open and run either notebook cell by cell ▶️
   - `Python Linear Search.ipynb`
   - `Python Binary Search.ipynb`

---

# 🌟 Key Highlights ⭐

✨ Both algorithms implemented purely through **Recursion**
🔍 **Linear Search** — works on any array, no sorting required
🔎 **Binary Search** — logarithmic efficiency, requires sorted input
🧠 Builds strong intuition for **base cases** and **recursive calls**
📊 Includes step-by-step trace of each recursive call

---

# 🛡️ Tech Stack 💻

![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)
![VS Code](https://img.shields.io/badge/VSCode-Editor-blue?style=for-the-badge&logo=visualstudiocode)

---

# 🤝 Contributing 💡

Fork 🍴 → Improve 🔧 → PR 🚀

All contributions are welcome — bug fixes, new test cases, or additional explanations.

---

# 📬 Contact 📧

Feel free to connect! 😊

---

# 🎉 Happy Coding! 🚀🐍🔍
