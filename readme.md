# 🌀 Maze Solver in Python

This project implements a **maze solver** using **Depth-First Search (DFS)** and **Breadth-First Search (BFS)** algorithms.
The solver reads a maze from a text file, explores nodes, and prints the maze with the solution path.

---

##  Project Structure

```
maze-solver/
│── maze.py        # Main program (solver code)
│── maze1.txt      # Sample maze with solution
│── maze2.txt      # Another maze file
│── README.md      # Project documentation
```

---

##  Features

* Solve mazes with **DFS** (default) or **BFS** (by swapping `StackFrontier` with `QueueFrontier`).
* Keeps track of **explored nodes**.
* Prints the maze with:

  * `A` → Start
  * `B` → Goal
  * `█` → Wall
  * `*` → Solution path
* Displays total nodes explored.

---

## Usage

### 1. Prepare a maze file

A maze is a **text file** where:

* `A` = Start
* `B` = Goal
* `█` or `#` = Walls
* Space (` `) = Empty path

Example (**maze1.txt**):

```
########
#A    B#
# #### #
#      #
########
```

### 2. Run the solver

```bash
python maze.py
```

Output:

```
########
#A****B#
# #### #
#      #
########

Totl Node Explored : 12
```

---

##  Switching Between DFS and BFS

By default, the solver uses **DFS**:

```python
frontier = StackFrontier()
```

To use **BFS**, replace with:

```python
frontier = QueueFrontier()
```

---

##  Example with Two Mazes

The script at the bottom solves **maze2.txt** and **maze1.txt**:

```python
if __name__ == "__main__":
    maze = Maze("maze2.txt")
    maze.solve()
    maze.print()

    maze1 = Maze("maze1.txt")
    maze1.solve()
    maze1.print()
```

---

##  Output Example

For a solvable maze:

```
█A***█
█ ** █
█ **B█
█    █
██████

Totl Node Explored : 18
```

---

##  Future Improvements

* Add **random maze generator**.
* Visualize solving process step by step.
* Compare DFS vs BFS efficiency.

---

 Developed with Python
