# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 28, 2026, 8:00 PM]
**What I did**: Initial review of the assignment requirements and setting up the environment.

**Details**: 
• Read the full assignment PDF to understand MultiThreading and Round-Robin simulation.
• Created a GitHub account using the university email.
• Forked the starter repository and renamed it to OS-Assignment1-Nada-Rashed-445

**Challenges**: Understanding the existing Process class and how the SchedulerSimulation handles the queue.

**Solution**: Carefully reviewed the code comments and the logic of run() and runToCompletion() methods. 

**Time spent**: 2 hours.

---

### Entry 2 - [April 1, 2026, 1:00 PM]
**What I did**: Personalizing the code and implementing Feature 1 (Priority).

**Details**:
• Updated studentID on line 210 of SchedulerSimulation.java to my actual ID.  
• Added a priority field (integer 1-5) to the Process class.  
• Modified the process creation logic to generate random priorities. 

**Challenges**: Ensuring the priority is displayed correctly when the process enters the ready queue. 

**Solution**: Updated the addProcessToQueue method to include the priority in the print statement. 

**Time spent**: 1.5 hours.

---

### Entry 3 - [April 1, 2026, 3:00 PM]
**What I did**: Implementing Feature 2 (Context Switches) and testing.

**Details**:
• Added a static counter variable to track context switches in SchedulerSimulation.  
• Incremented the counter every time a new process thread starts running.  
• Added a final print statement to show the total count at the end of the simulation. 

**Challenges**: Deciding exactly where to increment the counter to ensure it only counts actual switches.

**Solution**: Placed the increment logic inside the scheduler loop where a process is retrieved from the queue.

**Time spent**: 1 hour.

---

### Entry 4 - [April 2, 2026, 1:00 PM]
**What I did**: Implementing Feature 3 (Waiting Time Tracking).

**Details**: 
• Added fields for creationTime and totalWaitTime in the Process class.  
• Used System.currentTimeMillis() to calculate the time spent in the queue.  
• Created a summary table to display Name, Burst Time, and Waiting Time.

**Challenges**: Calculating wait time correctly when a process is re-enqueued multiple times. 

**Solution**: Tracked the time a process finishes its quantum and subtracted it from the next start time.

**Time spent**: 3 hours.

---

### Entry 5 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [X hours]

**Most challenging part**: 

**Most interesting learning**: 

**What I would do differently next time**: 
