# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

A process is an independent program in execution with its own dedicated memory and resources, completely isolated from other processes, while a thread is a small execution unit within a single process. We used threads in this assignment because they share the same memory and resources as the parent process, making communication between them faster and less resource-intensive than creating separate processes. The effectiveness of threads is demonstrated in our simulation within the SchedulerSimulation.java file, where we were able to manage multiple tasks (such as the P1 and P2 dummy processes) within a single program with minimal creation overhead. This distinction is crucial in operating systems because threads allow us to achieve highly efficient parallelism without the need for complex data-sharing mechanisms between processes.

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

In the Round-Robin scheduling algorithm, when a process fails to complete its full burst time within its allotted time quota, it is temporarily suspended, freeing up processor resources for the next process. The scheduler then re-inserts this process at the end of the Ready Queue to ensure all other processes have an opportunity to execute. This behavior ensures fairness in the allocation of processor resources and prevents any long-running process from monopolizing the system.

Example from my output:

[P1] executing quantum [4000ms]
Quantum progress:[####################] 100%
P1 completed quantum 4000ms | Overall progress: [##########----------] 56%
Remaining time: 3121ms
P1 yields CPU for context switch

P1 (Priority: 4) added to ready queue | Burst time: 7121ms
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

The example above shows that process P1 exhausted its 4000 milliseconds time quota, and with 3121 milliseconds remaining, a "yields CPU" message appeared, indicating that it was releasing the processor. Immediately afterward, the system added it back to the end of the queue (added to ready queue) while maintaining its priority (Priority:4). This move allows the next process in the queue (P2) to begin execution, thus maintaining system responsiveness and balance.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

In our simulation, the thread of the process (such as P1) goes through several states, starting from the New state when the thread object is created in the addProcessToQueue function and before Thread.start() is called. The thread goes to the Runnable state as soon as the start() function is called, where it becomes ready to execute and waits in the Ready Queue. When the scheduler selects it and grants it access to the processor, it enters the Running state and begins executing the run() function. It may also go to the Waiting (or timed) state when Thread.sleep() is called to simulate execution time. Finally, the thread enters the Terminated state after the Burst Time has fully completed and the run() function has finished executing, or after Thread.join() is called in the main code to wait for the tasks to finish.

1. **New**: [When is P1 in New state?]
 P1 in this case is when the new Thread(process) object is created in the addProcessToQueue function before it is activated. 

2. **Runnable**: [When does P1 become Runnable?]
In this case, P1 becomes immediately upon calling Thread.start(); it is ready to work and is waiting its turn in the queue.

3. **Running**: [When is P1 Running?]
P1 enters the run state when the scheduler pulls it from the queue and allocates the processor to it to begin executing the run() function.

4. **Waiting**: [When/why would P1 be Waiting?]
P1 switches to this state (Timed Waiting) while Thread.sleep() is being called to simulate time consumption, or when waiting for other threads.

5. **Terminated**: [When is P1 Terminated?]
P1 ends and reaches this state when its execution is fully completed and the remainingTime equals zero.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Servers]

**Description**: 
[Describe the real-world scenario or application]

Web servers, such as those that run e-commerce sites, use multi-reading to process requests from thousands of users at the same time.

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

This algorithm ensures fair CPU time allocation among all user requests, preventing a single, heavy request from disrupting the rest. This maintains the site's responsiveness for everyone, just as seen in the simulation where each process received a specific time allocation before being given over to others.

### Example 2: [Media Players]

**Description**: 
[Describe the real-world scenario or application]

In Media Players applications, separate tracks are used to process audio, image, and download data from the internet to ensure a smooth, uninterrupted display.

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

This is ideal because it offers predictability in execution, with each track receiving a periodic time to ensure audio and video synchronization. Implementing the "context switching" concepts we programmed in the second feature ensures the processor quickly switches between these tasks, making them appear to the user as if they are working simultaneously.

---

## Summary

**Key concepts I understood through these questions:**
1. The fundamental difference between a process and a thread in terms of resource consumption.
2. How to manage the thread lifecycle programmatically.
3. The importance of scheduling fairness in improving system performance.

**Concepts I need to study more:**
1. How to handle "Thread Synchronization" to avoid data interference.
2. Advanced scheduling algorithms that rely on dynamic priorities rather than randomness.
