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
- 🔍 Linear Search - Recursive Flowchart
- 🔎 Binary Search - Recursive Flowchart
- ⚡ Complexity Comparison
- ⚙️ How to Use
- 🌟 Key Highlights
- 🤝 Contributing
- 📬 Contact

---

# 📖 Introduction ✨

This repository is **Part 4** of the Python Advance Complete Tutorial series.

It covers **Searching Algorithms** implemented entirely through **Recursion** - reinforcing both algorithmic thinking and recursive problem solving simultaneously.

You will learn:
- How to recursively scan every element to find a target (Linear Search)
- How to recursively halve the search space to find a target (Binary Search)

---

# 📂 Repository Structure 🗂️

```
├──📄 README.md
📂 Python_Advance_Complete_Tutorial_Part_4/
└── 📂 Searching Algorithms in Python/
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

<svg viewBox="0 0 420 520" xmlns="http://www.w3.org/2000/svg" width="420" height="520" style="font-family:Arial,sans-serif;background:#f9f9f9;border-radius:10px;">
  <!-- Title -->
  <text x="210" y="30" text-anchor="middle" font-size="13" font-weight="bold" fill="#1a1a2e">linear_search(arr, target, i)</text>

  <!-- Start box -->
  <rect x="110" y="45" width="200" height="40" rx="20" ry="20" fill="#4A90D9" stroke="#2c6fad" stroke-width="1.5"/>
  <text x="210" y="70" text-anchor="middle" font-size="12" fill="white" font-weight="bold">START CALL</text>

  <!-- Arrow down -->
  <line x1="210" y1="85" x2="210" y2="110" stroke="#555" stroke-width="1.5" marker-end="url(#arrow)"/>

  <!-- Diamond: i >= len(arr) -->
  <polygon points="210,115 310,150 210,185 110,150" fill="#FFF3CD" stroke="#e0a800" stroke-width="1.5"/>
  <text x="210" y="146" text-anchor="middle" font-size="11" fill="#333">i &gt;= len(arr)?</text>

  <!-- YES branch (right) -->
  <line x1="310" y1="150" x2="370" y2="150" stroke="#555" stroke-width="1.5" marker-end="url(#arrow)"/>
  <text x="340" y="144" text-anchor="middle" font-size="10" fill="#c0392b" font-weight="bold">Yes</text>
  <rect x="370" y="130" width="38" height="38" rx="5" fill="#F28B82" stroke="#c0392b" stroke-width="1.5"/>
  <text x="389" y="153" text-anchor="middle" font-size="11" fill="#7b0000" font-weight="bold">-1</text>

  <!-- NO branch (down) -->
  <line x1="210" y1="185" x2="210" y2="215" stroke="#555" stroke-width="1.5" marker-end="url(#arrow)"/>
  <text x="222" y="205" font-size="10" fill="#27ae60" font-weight="bold">No</text>

  <!-- Diamond: arr[i] == target -->
  <polygon points="210,220 310,255 210,290 110,255" fill="#FFF3CD" stroke="#e0a800" stroke-width="1.5"/>
  <text x="210" y="251" text-anchor="middle" font-size="11" fill="#333">arr[i] == target?</text>

  <!-- YES branch (right) -->
  <line x1="310" y1="255" x2="370" y2="255" stroke="#555" stroke-width="1.5" marker-end="url(#arrow)"/>
  <text x="340" y="249" text-anchor="middle" font-size="10" fill="#c0392b" font-weight="bold">Yes</text>
  <rect x="370" y="235" width="38" height="38" rx="5" fill="#81C995" stroke="#1e8449" stroke-width="1.5"/>
  <text x="389" y="258" text-anchor="middle" font-size="11" fill="#145a32" font-weight="bold">i</text>

  <!-- NO branch (down) -->
  <line x1="210" y1="290" x2="210" y2="320" stroke="#555" stroke-width="1.5" marker-end="url(#arrow)"/>
  <text x="222" y="310" font-size="10" fill="#27ae60" font-weight="bold">No</text>

  <!-- Recurse box -->
  <rect x="85" y="320" width="250" height="42" rx="6" fill="#D0E8FF" stroke="#4A90D9" stroke-width="1.5"/>
  <text x="210" y="336" text-anchor="middle" font-size="11" fill="#1a3a5c">Recurse:</text>
  <text x="210" y="353" text-anchor="middle" font-size="11" fill="#1a3a5c" font-weight="bold">linear_search(arr, target, i+1)</text>

  <!-- Loop back arrow -->
  <line x1="85" y1="341" x2="55" y2="341" stroke="#555" stroke-width="1.5"/>
  <line x1="55" y1="341" x2="55" y2="65" stroke="#555" stroke-width="1.5"/>
  <line x1="55" y1="65" x2="110" y2="65" stroke="#555" stroke-width="1.5" marker-end="url(#arrow)"/>

  <!-- Initial call note -->
  <rect x="60" y="430" width="300" height="34" rx="8" fill="#eef7ff" stroke="#4A90D9" stroke-width="1"/>
  <text x="210" y="450" text-anchor="middle" font-size="11" fill="#1a3a5c">📌 Initial call:</text>
  <text x="210" y="465" text-anchor="middle" font-size="11" fill="#1a3a5c" font-weight="bold">linear_search(arr, target, 0)</text>

  <defs>
    <marker id="arrow" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto">
      <path d="M0,0 L0,6 L8,3 z" fill="#555"/>
    </marker>
  </defs>
</svg>

> **Initial call:** `linear_search(arr, target, 0)`

---

# 🔎 Binary Search — Recursive Flowchart 📊

Binary Search eliminates half the search space at each recursive call. It requires a sorted array. At each call: compute `mid`, check base cases, then recurse either left (`hi = mid - 1`) or right (`lo = mid + 1`).

<svg viewBox="0 0 520 620" xmlns="http://www.w3.org/2000/svg" width="520" height="620" style="font-family:Arial,sans-serif;background:#f9f9f9;border-radius:10px;">
  <!-- Title -->
  <text x="260" y="28" text-anchor="middle" font-size="13" font-weight="bold" fill="#1a1a2e">binary_search(arr, target, lo, hi)</text>

  <!-- Start box -->
  <rect x="140" y="40" width="240" height="38" rx="19" ry="19" fill="#4A90D9" stroke="#2c6fad" stroke-width="1.5"/>
  <text x="260" y="63" text-anchor="middle" font-size="12" fill="white" font-weight="bold">START CALL</text>

  <!-- Arrow down -->
  <line x1="260" y1="78" x2="260" y2="100" stroke="#555" stroke-width="1.5" marker-end="url(#arrow2)"/>

  <!-- Compute mid box -->
  <rect x="155" y="100" width="210" height="36" rx="6" fill="#E8D5FF" stroke="#7b2fbe" stroke-width="1.5"/>
  <text x="260" y="122" text-anchor="middle" font-size="12" fill="#4a0072" font-weight="bold">mid = (lo + hi) // 2</text>

  <!-- Arrow down -->
  <line x1="260" y1="136" x2="260" y2="160" stroke="#555" stroke-width="1.5" marker-end="url(#arrow2)"/>

  <!-- Diamond: lo > hi -->
  <polygon points="260,165 370,200 260,235 150,200" fill="#FFF3CD" stroke="#e0a800" stroke-width="1.5"/>
  <text x="260" y="196" text-anchor="middle" font-size="11.5" fill="#333">lo &gt; hi?</text>

  <!-- YES branch (right) -->
  <line x1="370" y1="200" x2="440" y2="200" stroke="#555" stroke-width="1.5" marker-end="url(#arrow2)"/>
  <text x="407" y="193" text-anchor="middle" font-size="10" fill="#c0392b" font-weight="bold">Yes</text>
  <rect x="440" y="180" width="40" height="38" rx="5" fill="#F28B82" stroke="#c0392b" stroke-width="1.5"/>
  <text x="460" y="203" text-anchor="middle" font-size="12" fill="#7b0000" font-weight="bold">-1</text>

  <!-- NO branch (down) -->
  <line x1="260" y1="235" x2="260" y2="265" stroke="#555" stroke-width="1.5" marker-end="url(#arrow2)"/>
  <text x="272" y="256" font-size="10" fill="#27ae60" font-weight="bold">No</text>

  <!-- Diamond: arr[mid] == target -->
  <polygon points="260,270 380,305 260,340 140,305" fill="#FFF3CD" stroke="#e0a800" stroke-width="1.5"/>
  <text x="260" y="301" text-anchor="middle" font-size="11.5" fill="#333">arr[mid] == target?</text>

  <!-- YES branch (right) -->
  <line x1="380" y1="305" x2="440" y2="305" stroke="#555" stroke-width="1.5" marker-end="url(#arrow2)"/>
  <text x="412" y="298" text-anchor="middle" font-size="10" fill="#c0392b" font-weight="bold">Yes</text>
  <rect x="440" y="285" width="50" height="38" rx="5" fill="#81C995" stroke="#1e8449" stroke-width="1.5"/>
  <text x="465" y="308" text-anchor="middle" font-size="12" fill="#145a32" font-weight="bold">mid</text>

  <!-- NO branch (down) -->
  <line x1="260" y1="340" x2="260" y2="368" stroke="#555" stroke-width="1.5" marker-end="url(#arrow2)"/>
  <text x="272" y="360" font-size="10" fill="#27ae60" font-weight="bold">No</text>

  <!-- Diamond: arr[mid] < target -->
  <polygon points="260,373 380,408 260,443 140,408" fill="#FFF3CD" stroke="#e0a800" stroke-width="1.5"/>
  <text x="260" y="404" text-anchor="middle" font-size="11.5" fill="#333">arr[mid] &lt; target?</text>

  <!-- YES branch (right): lo = mid+1 -->
  <line x1="380" y1="408" x2="430" y2="408" stroke="#555" stroke-width="1.5" marker-end="url(#arrow2)"/>
  <text x="407" y="401" text-anchor="middle" font-size="10" fill="#c0392b" font-weight="bold">Yes</text>
  <rect x="430" y="388" width="78" height="38" rx="5" fill="#D0E8FF" stroke="#4A90D9" stroke-width="1.5"/>
  <text x="469" y="407" text-anchor="middle" font-size="10.5" fill="#1a3a5c">Recurse:</text>
  <text x="469" y="420" text-anchor="middle" font-size="10" fill="#1a3a5c" font-weight="bold">lo=mid+1</text>

  <!-- NO branch (left): hi = mid-1 -->
  <line x1="140" y1="408" x2="90" y2="408" stroke="#555" stroke-width="1.5" marker-end="url(#arrow2)"/>
  <text x="115" y="401" text-anchor="middle" font-size="10" fill="#c0392b" font-weight="bold">No</text>
  <rect x="12" y="388" width="78" height="38" rx="5" fill="#D0E8FF" stroke="#4A90D9" stroke-width="1.5"/>
  <text x="51" y="407" text-anchor="middle" font-size="10.5" fill="#1a3a5c">Recurse:</text>
  <text x="51" y="420" text-anchor="middle" font-size="10" fill="#1a3a5c" font-weight="bold">hi=mid-1</text>

  <!-- Loop back arrow from right box -->
  <line x1="469" y1="388" x2="469" y2="63" stroke="#aaa" stroke-width="1.2" stroke-dasharray="5,3"/>
  <line x1="469" y1="63" x2="380" y2="63" stroke="#aaa" stroke-width="1.2" stroke-dasharray="5,3" marker-end="url(#arrow2)"/>

  <!-- Loop back arrow from left box -->
  <line x1="51" y1="388" x2="51" y2="63" stroke="#aaa" stroke-width="1.2" stroke-dasharray="5,3"/>
  <line x1="51" y1="63" x2="140" y2="63" stroke="#aaa" stroke-width="1.2" stroke-dasharray="5,3" marker-end="url(#arrow2)"/>

  <!-- Initial call note -->
  <rect x="80" y="530" width="360" height="36" rx="8" fill="#eef7ff" stroke="#4A90D9" stroke-width="1"/>
  <text x="260" y="550" text-anchor="middle" font-size="11" fill="#1a3a5c">📌 Initial call:</text>
  <text x="260" y="566" text-anchor="middle" font-size="11" fill="#1a3a5c" font-weight="bold">binary_search(arr, target, 0, len(arr) - 1)</text>

  <defs>
    <marker id="arrow2" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto">
      <path d="M0,0 L0,6 L8,3 z" fill="#555"/>
    </marker>
  </defs>
</svg>

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

