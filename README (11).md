<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=DSA%20Java%20Masterclass&fontSize=50&fontColor=fff&animation=twinkling&fontAlignY=35&desc=Algorithms%20%26%20Data%20Structures%20in%20Java&descAlignY=55&descSize=18"/>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=00D9FF&center=true&vCenter=true&multiline=true&width=700&height=100&lines=🧠+BFS+%7C+DFS+%7C+A*+Search+%7C+Dynamic+Programming;⚡+Clean+Code+%7C+Well+Commented+%7C+Interview+Ready;🚀+Built+with+Pure+Java+%7C+No+Dependencies)](https://git.io/typing-svg)

<br/>

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Algorithms](https://img.shields.io/badge/Algorithms-007396?style=for-the-badge&logo=thealgorithms&logoColor=white)
![DSA](https://img.shields.io/badge/Data%20Structures-FF6B6B?style=for-the-badge&logo=databricks&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

<br/>

![GitHub stars](https://img.shields.io/github/stars/satyahasinihasini-star/DSA-Java-Masterclass?style=social)
![GitHub forks](https://img.shields.io/github/forks/satyahasinihasini-star/DSA-Java-Masterclass?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/satyahasinihasini-star/DSA-Java-Masterclass?style=social)

</div>

---

<div align="center">

## 🌟 What is this project?

</div>

> **DSA Java Masterclass** is a comprehensive, production-quality collection of **Data Structures & Algorithms** implemented in Java. Every algorithm is clean, well-commented, and ready for **coding interviews**, **university exams**, or **learning from scratch**.

---

## 📊 Algorithms at a Glance

<div align="center">

| Category | Algorithm | Time Complexity | Space Complexity | Difficulty |
|:---:|:---:|:---:|:---:|:---:|
| 🔵 Graph | BFS | `O(V + E)` | `O(V)` | 🟢 Easy |
| 🔵 Graph | DFS (Recursive + Iterative) | `O(V + E)` | `O(V)` | 🟢 Easy |
| 🔴 Pathfinding | A\* Search | `O(E log V)` | `O(V)` | 🔴 Hard |
| 🟡 DP | Fibonacci (3 methods) | `O(n)` | `O(1)` | 🟢 Easy |
| 🟡 DP | 0/1 Knapsack | `O(n × W)` | `O(n × W)` | 🟠 Medium |
| 🟡 DP | Longest Common Subsequence | `O(m × n)` | `O(m × n)` | 🟠 Medium |

</div>

---

## 📁 Project Structure

```
📦 DSA-Java-Masterclass
 ┣ 📂 src
 ┃ ┣ 📂 algorithms
 ┃ ┃ ┣ 📂 graph
 ┃ ┃ ┃ ┣ 📜 BFS.java              ← Breadth-First Search
 ┃ ┃ ┃ ┣ 📜 DFS.java              ← Depth-First Search (Recursive + Iterative)
 ┃ ┃ ┃ └ 📜 AStarSearch.java      ← A* Grid Pathfinding
 ┃ ┃ └ 📂 dynamic
 ┃ ┃   ┣ 📜 Fibonacci.java        ← 3 DP Approaches
 ┃ ┃   ┣ 📜 Knapsack.java         ← 0/1 Knapsack + Item Backtracking
 ┃ ┃   └ 📜 LongestCommonSubsequence.java
 ┃ └ 📂 main
 ┃   └ 📜 Main.java               ← Demo Runner
 ┣ 📜 .gitignore
 └ 📜 README.md
```

---

## 🚀 Quick Start

### ✅ Prerequisites
```bash
java --version   # Java 8 or higher required
```

### 📥 Clone the Repository
```bash
git clone https://github.com/satyahasinihasini-star/DSA-Java-Masterclass.git
cd DSA-Java-Masterclass
```

### ⚙️ Compile & Run All
```bash
cd src
javac algorithms/graph/*.java algorithms/dynamic/*.java main/Main.java
java main.Main
```

### ▶️ Run Individual Algorithms
```bash
java algorithms.graph.BFS
java algorithms.graph.DFS
java algorithms.graph.AStarSearch
java algorithms.dynamic.Knapsack
java algorithms.dynamic.LongestCommonSubsequence
java algorithms.dynamic.Fibonacci
```

---

## 💡 Algorithm Explanations

<details>
<summary>🔵 <b>BFS — Breadth-First Search</b></summary>

<br/>

BFS explores a graph **level by level** using a **Queue**.

```
Graph:    0
         / \
        1   2
        |   |
        3   4
        |
        5
```

**BFS from 0:** `[0] → [1, 2] → [3, 4] → [5]`

- ✅ Finds **shortest path** in unweighted graphs
- ✅ Used in social networks, GPS, web crawlers
- ✅ Includes **connectivity check** between nodes

</details>

<details>
<summary>🔵 <b>DFS — Depth-First Search</b></summary>

<br/>

DFS explores as **deep as possible** before backtracking.

- 📌 **Recursive version** — uses call stack
- 📌 **Iterative version** — uses explicit Stack
- 📌 **Cycle Detection** — detects if graph has a cycle

```java
// Recursive core
void dfsHelper(int node, boolean[] visited) {
    visited[node] = true;
    for (int neighbor : adjList[node])
        if (!visited[neighbor])
            dfsHelper(neighbor, visited);
}
```

</details>

<details>
<summary>🔴 <b>A* Search — Heuristic Pathfinding</b></summary>

<br/>

A* finds the **optimal path** on a 2D grid using:

```
f(n) = g(n) + h(n)
       ↑         ↑
  cost so far   heuristic (Manhattan Distance)
```

**Grid Example:**
```
S . . . .        S = Start (0,0)
. X X X .        E = End   (4,4)
. . . X .        X = Wall/Obstacle
. X . . .
. . . X E
```

A* navigates around walls to find the **shortest valid path**!

</details>

<details>
<summary>🟡 <b>Dynamic Programming — Fibonacci</b></summary>

<br/>

Three approaches compared:

| Approach | Time | Space | Method |
|---|---|---|---|
| Memoization | O(n) | O(n) | Top-Down Recursion |
| Tabulation | O(n) | O(n) | Bottom-Up Table |
| Optimized | O(n) | **O(1)** | Two Variables |

```java
// Space Optimized — Best approach
long a = 0, b = 1;
for (int i = 2; i <= n; i++) {
    long c = a + b;
    a = b; b = c;
}
```

</details>

<details>
<summary>🟡 <b>Dynamic Programming — 0/1 Knapsack</b></summary>

<br/>

**Problem:** Given items with weights & values, maximize value within a weight capacity.

```
Items:    Weight  Value
  A         2      3
  B         3      4
  C         4      5
  D         5      6

Capacity = 8
Best pick: A + B + C → Value = 12  ✅
```

Uses a 2D DP table + **backtracking** to find selected items.

</details>

<details>
<summary>🟡 <b>Dynamic Programming — LCS</b></summary>

<br/>

**Longest Common Subsequence** of two strings.

```
s1 = "ABCBDAB"
s2 = "BDCAB"

LCS = "BCAB"  (length = 4)
```

Returns both the **length** and the **actual subsequence string**.

</details>

---

## 🖥️ Sample Output

```
==========================================
   ADS — Algorithms & Data Structures     
==========================================

[ BFS - Breadth-First Search ]
  Traversal from 0 : [0, 1, 2, 3, 4, 5]
  0 connected to 5 : true

[ DFS - Depth-First Search ]
  Recursive : [0, 1, 3, 5, 2, 4]
  Iterative : [0, 2, 4, 1, 3, 5]
  Has Cycle : false

[ A* Search - Grid Pathfinding ]
  Path found: true (9 steps)

[ 0/1 Knapsack - Dynamic Programming ]
  Max value (capacity=8): 9

[ LCS - Longest Common Subsequence ]
  LCS of ABCBDAB & BDCAB: BCAB

[ Fibonacci - DP ]
  Fib(10) = 55

==========================================
              All Done! ✅                
==========================================
```

---

## 🛠️ IDE Setup

<details>
<summary>💜 <b>IntelliJ IDEA</b></summary>

1. `File > Open` → select the `DSA-Java-Masterclass` folder
2. Right-click `src` → `Mark Directory as > Sources Root`
3. Run `Main.java` ▶️

</details>

<details>
<summary>🔵 <b>VS Code</b></summary>

1. Install **Extension Pack for Java**
2. Open the project folder
3. Click ▶️ on `Main.java`

</details>

<details>
<summary>🟠 <b>Eclipse</b></summary>

1. `File > New > Java Project`
2. Uncheck default location → point to project folder
3. Run `Main.java`

</details>

---

## 🗺️ Roadmap

- [x] 🔵 BFS — Breadth-First Search
- [x] 🔵 DFS — Depth-First Search
- [x] 🔴 A\* Search
- [x] 🟡 Fibonacci (3 DP methods)
- [x] 🟡 0/1 Knapsack
- [x] 🟡 Longest Common Subsequence
- [ ] 🔜 Dijkstra's Algorithm
- [ ] 🔜 Bellman-Ford
- [ ] 🔜 Merge Sort / Quick Sort
- [ ] 🔜 Binary Search Variants
- [ ] 🔜 Tree Traversals (Inorder, Preorder, Postorder)
- [ ] 🔜 Heap / Priority Queue
- [ ] 🔜 Graph — Topological Sort
- [ ] 🔜 String — KMP Pattern Matching

---

## 🤝 Contributing

Contributions are welcome! Here's how:

```bash
# 1. Fork the repo
# 2. Create your branch
git checkout -b feature/your-algorithm

# 3. Commit your changes
git commit -m "Add: YourAlgorithm with explanation"

# 4. Push to GitHub
git push origin feature/your-algorithm

# 5. Open a Pull Request 🎉
```

**Guidelines:**
- Add javadoc comments with Time & Space complexity
- Include a `main()` method with a working demo
- Keep code clean and readable

---

## 📄 License

```
MIT License — Free to use, learn, and modify.
```

---

<div align="center">

### 🌟 If this helped you, please give it a Star!

[![Star History Chart](https://api.star-history.com/svg?repos=satyahasinihasini-star/DSA-Java-Masterclass&type=Date)](https://star-history.com/#satyahasinihasini-star/DSA-Java-Masterclass&Date)

<br/>

**Made with ❤️ and ☕ by [satyahasinihasini-star](https://github.com/satyahasinihasini-star)**

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer"/>

</div>
