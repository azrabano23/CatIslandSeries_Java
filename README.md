# CatIsland

# 🏝️ Island Simulation – SmartCat on Randomly Generated Terrains  
_A Java OOP and Algorithms Project by Azra Bano · Rutgers University_

This simulation models a randomized island environment where autonomous cats navigate land tiles, collect yarn, and solve mazes using graph algorithms. It's built with a strong foundation in object-oriented design, recursion, and data structures like trees, queues, and hash maps.

---

## 🧠 Project Highlights

### 🎯 SmartCat (Core Agent Logic)
`SmartCat` extends the base `Cat` class with intelligent pathfinding and recursive maze-solving features.

- **`walkPath()`** – Recursively traverses a narrow land path without backtracking  
- **`collectAllYarn()`** – Filters reachable yarn using **BFS**, navigates via **Manhattan distance**  
- **`solveMaze()`** – Navigates to the exit using DFS + path-checking heuristics  
- **`navigateTo()`** – Implements a **BFS shortest path** to a target `Tile`  
- **`hasPathTo()`** – Returns all reachable yarn tiles from the cat’s current position  

---

## 🏗️ Random Island Generation
The `RandomCatIsland` engine builds a procedural island layout based on a user’s NetID seed.

### 🌍 Features
- **Random land/water tile matrix (9x9 – 12x12)**  
- **Random yarn spawn rate (25% land fill)**  
- **Procedural path connection using a central hub**  
- **Cat placement with spatial deconfliction logic**  
- **Seeded randomness via ASCII-hashed NetID**

### 🐈 Cat Movement
- Each turn, all cats move with 75% probability  
- Movement uses 4-directional trial with land validation  
- Yarn spawns with 1/10 chance each round, placed only if no nearby yarn exists  

---

## 🧪 Algorithms in Use

| Feature               | Algorithm / Technique           |
|------------------------|------------------------------|
| Path to Yarn           | BFS, adjacency validation     |
| Yarn Targeting         | Manhattan Distance Heuristic |
| Maze Solving           | DFS with reachability checks |
| Land Connectivity      | Multi-source to hub pathing  |
| Yarn Placement         | Probabilistic sampling with 8-tile radius check |
| Cat Movement           | Probabilistic greedy random walk |

---

## 🛠️ Technologies
- **Language**: Java  
- **Paradigms**: OOP, Recursion, Simulation, BFS/DFS  
- **Utility Libraries**: `HashMap`, `Queue`, `Set`, `StdRandom` (custom RNG)

---

## 📸 Example Use Case

```java
SmartCat azra = new SmartCat("Azra", island, 2, 3, Color.BLACK);
azra.collectAllYarn();   // Greedily gathers all reachable yarn
azra.solveMaze();        // Escapes maze by navigating to top-right tile
```

---

## ❓ Sample Game Questions Generator

The system auto-generates island-specific quiz-style questions for testing comprehension:

- "How many yarn were on the island at time=183?"  
- "What row was Cat3 in at time=221?"  
- "What is the most yarn a single cat collected?"

---

## 🔍 Key Concepts Reinforced

✅ Recursion  
✅ Object-Oriented Inheritance  
✅ BFS & DFS in Grid Graphs  
✅ State-based Simulation  
✅ Procedural World Generation  
✅ Queue + HashSet Traversals  
✅ Greedy Search & Pathfinding  

---

## 👨‍💻 Author

**Azra Bano** – Rutgers University  
_Software Engineer · AI Systems Researcher · OOP Simulation Enthusiast_  
📫 [azra-bano.com](https://azra-bano.com) • [LinkedIn](https://linkedin.com/in/meetazrabano)  

---

## 📄 License

This project is for educational and portfolio use. All algorithms are original unless noted.
