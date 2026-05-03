#  print-scheduler-and-browser-navigation

A collection of classic data structure problems implemented in pure C++ for educational purposes. Built by  [Omar Ashraf](https://github.com/omarrashraff)
 &  [Mohamed Ahmed](https://github.com/minshawi0)


---

## Tasks

### Task 1 — Print Job Scheduler (Priority Queue)
A C++ implementation of a printer job scheduler using a **linked-list-based Priority Queue**. Jobs are read from a `printer.txt` file, sorted by arrival time (and duration as a tie-breaker), then executed in order. The system tracks and reports each job's waiting time, the printer's total occupation time, and the average waiting time across all jobs.

Key features:
- Parses job data (`PC name`, `arrival time`, `duration`) from a text file
- Converts arrival times between `hh:mm` string format and integer minutes
- Inserts jobs in sorted order using a custom `enqueue()` method
- Skips and reports any malformed lines in the input file
- Calculates and displays per-job wait time, total occupation time, and average wait

---

### Task 2 — Browser Navigation (Stack)
A C++ simulation of browser **Back** and **Forward** navigation using two stacks built on a singly linked list. URLs are loaded from a `URLs.txt` file and a sequence of navigation commands (`Backward` / `Forward`) is processed, displaying the current page, next page, and previous page after each command.

Key features:
- Reads up to 9 URLs from file and loads them into a `Backward` navigation stack
- Processes up to 10 navigation commands from the same file
- Maintains current page state and two stacks for bidirectional navigation
- Displays current, next, and previous pages after every command
- Handles invalid commands gracefully with a skip message

---

## Structure

```
data-structures-cpp/
├── Task1-PrintQueue/
│   ├── main.cpp        # Priority queue scheduler — PrintJob, Node, PriorityQueue
│   └── printer.txt     # Input file: one job per line (PCname hh:mm duration)
└── Task2-BrowserNav/
    ├── main.cpp        # Stack-based browser navigation — Node, Stack
    └── URLs.txt        # Input file: 9 URLs + 1 line of space-separated commands
```

---

## Input File Formats

**`printer.txt`** (Task 1)
```
PCname HH:MM duration
PC1 08:30 15
PC2 08:45 10
PC3 09:00 20
```

**`URLs.txt`** (Task 2)
```
https://google.com
https://github.com
https://stackoverflow.com
... (9 URLs total)
Backward Forward Backward Forward Backward Forward Backward Forward Backward Forward
```

---

## How to Run

### Prerequisites
- A C++ compiler supporting C++11 or later (e.g. `g++`, `clang++`)

### Task 1

```bash
g++ -o printqueue Task1-PrintQueue/main.cpp
./printqueue
```

### Task 2

```bash
g++ -o browsernav Task2-BrowserNav/main.cpp
./browsernav
```

> Make sure `printer.txt` and `URLs.txt` are in the same directory as the compiled executable.

---

## Purpose

These implementations are built for learning and understanding the mathematical and logical foundations behind classic data structures. No external libraries are used — everything is implemented from scratch using raw pointers and linked lists.

---

## Author

## Authors

- [Omar Ashraf](https://github.com/omarrashraff)
- [Mohamed Ahmed](https://github.com/minshawi0)
