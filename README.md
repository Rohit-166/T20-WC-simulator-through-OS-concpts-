#  T20 World Cup 2026 Simulator using Operating System Concepts

A multithreaded T20 cricket match simulator developed in **C++** to demonstrate practical applications of **Operating System concepts** such as CPU Scheduling, Thread Synchronization, Deadlock Detection, Resource Allocation Graphs, Semaphores, Mutexes, and Round Robin Scheduling.

The simulator models an India vs Australia T20 innings where players and match events behave like processes competing for system resources.

---

##  Overview

This project combines cricket simulation with core Operating System concepts. The match is executed using concurrent threads, synchronization primitives, scheduling algorithms, and deadlock handling mechanisms to mimic real OS behavior in an engaging and interactive way.

---

##  Features

- Complete T20 innings simulation (20 overs)
- Realistic ball-by-ball match execution
- Multithreaded architecture using POSIX Threads
- FCFS (First Come First Serve) batting scheduler
- SJF (Shortest Job First) batting scheduler
- Round Robin scheduling for bowlers
- Deadlock detection using Resource Allocation Graph (RAG)
- Run-out simulation through deadlock resolution
- Synchronization using mutexes, semaphores, and condition variables
- Dynamic batting and bowling scorecards
- Gantt chart generation for delivery execution timeline
- Wait-time comparison between FCFS and SJF scheduling

---

##  Operating System Concepts Implemented

### CPU Scheduling

#### FCFS (First Come First Serve)
Batsmen enter according to the natural batting order.

#### SJF (Shortest Job First)
Batsmen are scheduled based on estimated batting duration (balls faced).

The simulator compares:

- Average waiting time
- Middle-order waiting time
- Overall scheduling efficiency

### Multithreading

The simulation creates independent threads for:

- Batsmen
- Bowlers
- Fielders

allowing concurrent execution similar to processes in an operating system.

### Synchronization

To prevent race conditions, the simulator uses:

- Mutex Locks
- Semaphores
- Condition Variables

for safe access to shared resources such as:

- Scoreboard
- Batting order
- Match state
- Resource allocation graph

### Deadlock Detection & Recovery

A Resource Allocation Graph (RAG) is maintained throughout the simulation.

During run-out situations:

1. Resources (creases) are allocated to batsmen.
2. Cycles are detected in the graph.
3. Deadlocks are resolved by terminating one process (run out).

This demonstrates classic deadlock detection and recovery techniques used in Operating Systems.

### Round Robin Scheduling

Australian bowlers are scheduled using a Round Robin strategy.

Features include:

- Context Switching
- Over Allocation
- Death Over Prioritization
- Bowler Rotation

### Gantt Chart Visualization

Every delivery records:

- Start Time
- End Time
- Execution Duration
- Bowler
- Striker
- Ball Outcome

A Gantt-style timeline is generated to visualize execution flow.

---

##  Compilation

Compile using:

```bash
g++ -std=c++17 -Wall -pthread t20_simulator.cpp -o t20sim
```

Run:

```bash
./t20sim
```

---

##  Output Generated

The simulator produces:

- Ball-by-ball commentary
- Wicket events
- Run-out deadlock events
- Complete batting scorecard
- Bowling statistics
- Delivery timeline (Gantt Chart)
- FCFS vs SJF scheduling analysis

---

##  Learning Outcomes

This project demonstrates:

- Process and Thread Management
- CPU Scheduling Algorithms
- Synchronization Mechanisms
- Deadlock Detection and Recovery
- Resource Allocation Graphs
- Semaphores and Mutexes
- Concurrent Programming
- Performance Analysis

---

##  Technologies Used

- C++17
- POSIX Threads (pthread)
- Semaphores
- Mutexes
- Condition Variables
- STL Containers

---

##  Author

**Rohit Mahawar**  
IIT Roorkee

GitHub: https://github.com/Rohit-166

