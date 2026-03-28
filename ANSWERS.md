# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:Threads and processes are both units of execution, but they differ in how they use system resources. A process is an independent program with its own memory space, while a thread is a smaller unit that runs within a process and shares memory with other threads.

Processes require more time and resources to create because each one has its own memory and system resources. Threads, on the other hand, are lightweight and faster to create since they share the same memory space.

In this assignment, we used threads instead of processes because the simulation requires multiple tasks to run concurrently and interact efficiently. Threads allow faster context switching and better performance, making them more suitable for this type of scheduling simulation.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:In Round-Robin scheduling, if a process does not finish within its time quantum, it is moved back to the end of the ready queue. This ensures fairness, as all processes get equal chances to execute.

For example, when a process like P3 does not complete its execution within the given time quantum, it yields the CPU and is added again to the ready queue. Later, it will be scheduled again after other processes have had their turn.

Example from my output:P3 executing quantum [0ms]
Quantum progress: [██████████] 100%
P3 completed quantum 0ms
Remaining time: 9273ms
P3 yields CPU for context switch
P3 (Priority: 5) added to ready queue**
**Explanation of example:**

This output shows that process P3 was executing but did not finish within its time quantum. After completing its time slice, it yielded the CPU and was moved back to the ready queue. This behavior is part of Round-Robin scheduling, where each process gets equal time to execute. The process will wait for its next turn and will be scheduled again later.
[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]
A thread goes through several states during its lifecycle in the simulation. For process P1, we can track its movement through these states as follows:

1. **New**: P1 is in the New state when it is first created using the Thread constructor but has not started execution yet.

2. **Runnable**: After P1 is added to the ready queue and the thread is started, it enters the Runnable state, meaning it is ready to run when the CPU is available.

3. **Running**: P1 enters the Running state when the scheduler assigns it CPU time and it begins executing its task.

4. **Waiting**: P1 may enter the Waiting state when it yields the CPU after its time quantum ends or when it is waiting for its next turn in the ready queue.

5. **Terminated**: P1 reaches the Terminated state when it completes its execution and no longer needs CPU time.
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**
### Example 1: Operating System Task Scheduling

**Description**: 
Operating systems use scheduling algorithms to manage multiple running applications, such as browsers, music players, and background processes.

**Why Round-Robin works well here**: 
Round-Robin ensures fairness by giving each process a fixed time slice. This prevents any single process from monopolizing the CPU and keeps the system responsive for all applications.

### Example 2: Web Server Handling Multiple Requests

**Description**: 
A web server handles multiple client requests at the same time using threads.

**Why Round-Robin works well here**: 
Round-Robin allows each request to be processed for a short time before moving to the next. This improves responsiveness and ensures that all users receive service without long delays.

---

## Summary

**Key concepts I understood through these questions:**
1. Difference between threads and processes
2. How Round-Robin scheduling ensures fairness
3. Thread lifecycle and state transitions

**Concepts I need to study more:**
1. Advanced thread synchronization techniques
2. Performance optimization in scheduling algorithms
**Concepts I need to study more:**
1. 
2. 
