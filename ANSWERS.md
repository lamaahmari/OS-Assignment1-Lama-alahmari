# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:Although they are both execution units, threads and processes consume system resources differently. A thread is a smaller unit that operates inside a process and shares memory with other threads, whereas a process is an independent program with its own memory space.

Because each process has its own memory and system resources, creating them takes more time and money. On the other hand, because they share memory, threads are lighter and quicker to generate.

Because the simulation needs several tasks to run simultaneously and communicate effectively, we used threads rather than processes in this project. Threads are better suited for this kind of scheduling simulation because they enable quicker context switching and improved performance.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:A process in Round-Robin scheduling is pushed back to the end of the ready queue if it does not complete within its time quantum. This guarantees equity since every process has an equal opportunity to run.

For instance, a process such as P3 surrender the CPU and is re-added to the ready queue if it fails to finish its execution within the allotted time period. It will be rescheduled later, following the completion of other processes.
Example from my output:Quantum execution by P3 [0 ms]
Quantum advancement: 100%
P3 finished quantum 0 ms.
Time left: 9273 ms
For the context transition, P3 yields CPU.
P3 (Priority: 5) has been added to the ready queue.
**Explanation of example:**

This report demonstrates that although process P3 was running, it did not complete within the allotted time. It returned to the ready queue after yielding the CPU after finishing its time slice. Round-Robin scheduling, which gives each process an equal amount of time to run, includes this behaviour. The procedure will await its subsequent turn and be rescheduled at a later time.
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
Throughout its existence in the simulation, a thread travels through a number of states. We can follow process P1 as it moves through these states in the manner shown below:
[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]


1. **New**: When P1 is initially formed using the Thread constructor, it is in the New state and has not yet begun to execute.

2. **Runnable**: P1 reaches the Runnable state, which indicates that it is prepared to run when the CPU is available, after being put to the ready queue and the thread is launched.

3. **Running**: When P1 receives CPU time from the scheduler and starts working on its task, it enters the Running state.
4. **Waiting**:When P1 waits for its next turn in the ready queue or surrender the CPU when its time quantum expires, it may go into the Waiting state.

5. **Terminated**: When P1 has finished running and no longer requires CPU time, it enters the Terminated state..
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**
### Example 1: Task Scheduling for Operating Systems

**Description**: 
Scheduling algorithms are used by operating systems to control several active programs, including background processes, audio players, and browsers.

**Why Round-Robin works well here**: 
By allocating a predetermined time slice to each activity, Round-Robin assures fairness. This maintains the system responsive for all apps and stops any one process from controlling the CPU.

### Example 2: Managing Several Requests on a Web Server

**Description**: 
A web server uses threads to manage several client requests concurrently.

**Why Round-Robin works well here**: 
Before going on to the next request, Round-Robin lets each one be processed for a brief period of time. This guarantees that all users receive service without significant delays and enhances responsiveness.

---

## Summary

**Key concepts I understood through these questions:**
1. The distinction between processes and threads
2. How Round-Robin scheduling guarantees equity
3. State transitions and the thread lifetime
**Concepts I need to study more:**
1. Sophisticated methods for thread synchronisation
2. Optimising scheduling algorithms' performance
   
**Concepts I need to study more:**
1. 
2. 
