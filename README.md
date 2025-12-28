# CPUScheduler (Java)

A Java library for simulating and analyzing 6 core CPU scheduling algorithms. It calculates performance metrics and generates data for Gantt chart visualization.

## Algorithms Included

* **FCFS:** First Come First Serve
* **SJF:** Shortest Job First (Non-preemptive)
* **SRT:** Shortest Remaining Time (Preemptive)
* **PSN:** Priority (Non-preemptive)
* **PSP:** Priority (Preemptive)
* **RR:** Round Robin (Requires Time Quantum)

---

## Quick Start

```java
CPUScheduler fcfs = new FirstComeFirstServe();
fcfs.add(new Row("P1", 0, 5)); // Name, Arrival, Burst
fcfs.add(new Row("P2", 2, 4));

fcfs.process();

double avgWait = fcfs.getAverageWaitingTime();
List<Event> timeline = fcfs.getTimeline(); // For Gantt Chart

```
## Or simply run the main.java or GUI.java file

```
java main.java

java GUI.java
```

---

## Features

* **Metrics:** Automatically calculates Waiting Time and Turnaround Time for every process.
* **Timeline API:** Returns a list of `Event` objects (`startTime`, `finishTime`, `processName`) to easily draw execution timelines.
* **GUI Demo:** Includes a built-in **Java Swing** application to visualize algorithm performance side-by-side.

## Repository Structure

* `src/`: Logic for all 6 scheduling algorithms.
