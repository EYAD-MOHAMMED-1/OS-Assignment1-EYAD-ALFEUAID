# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer: A process is a stand-alone program that is running and has its own memory and system resources. A thread, on the other hand, is a smaller unit of execution.
Because starting a new process necessitates assigning additional memory and system resources, processes are heavy-weight. Because threads share memory within the same process, they are lightweight and quick to create.
Since the simulation calls for several activities to execute simultaneously with shared data, such the ready queue, we used threads rather than processes in this assignment. Using procedures would increase complexity and needless overhead.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer: The ready queue follows a FIFO (First-In, First-Out) order. Processes are executed from the front of the queue, and if a process does not finish within its time quantum, it is moved to the end of the queue. Completed processes are removed and not returned. This cycle continues until the ready queue becomes empty, ensuring fair CPU allocation among all processes.**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output: 
[P4 → P5 → P6 → P7 → ... → P18 → P2] 
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example: This shows that after executing, the process (P2) was moved to the end of the ready queue, confirming the FIFO behavior where unfinished processes are reinserted at the back.**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer: Based on the output, threads (processes) transition through several states during execution: **

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**:When a process is created.
  [When is P1 in New state?]

2. **Runnable**: When a process is added to the ready queue and waiting for CPU:
  Example:
  "P1 (Priority: 1) added to ready queue"  [When does P1 become Runnable?]

3. **Running**:When the process is executing on the CPU:
  Example:
  "P2 executing quantum [3000ms]"
  [When is P1 Running?]

4. **Waiting**: When the process is interrupted (preempted) and waits before getting CPU again:
  Example:
  "P2 yields CPU for context switch"
 [When/why would P1 be Waiting?]

5. **Terminated**: When the process finishes execution completely:
  Example:
  "P1 finished execution!" [When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server [Name of application/scenario]

**Description**: Several client requests are handled concurrently by a web server.

[Describe the real-world scenario or application]

**Why Round-Robin works well here**: By allocating a time slice to each request, Round-Robin guarantees fairness by preventing any one request from blocking others.

[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: Operating System CPU Scheduling
 [Name of application/scenario]

**Description**:  Multiple computer programs are scheduled by operating systems.
[Describe the real-world scenario or application]

**Why Round-Robin works well here**:  It enhances responsiveness for interactive users and gives all processes equitable CPU access.
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. The distinction between processes and threads
2. The operation of Round-Robin scheduling
3. The states and lifetime of threads

**Concepts I need to study more:**
1. Synchronization and deadlocks
2. Complex algorithms for scheduling
