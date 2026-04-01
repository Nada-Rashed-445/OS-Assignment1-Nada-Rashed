# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

[Write your answer here. Discuss specific concepts like thread creation, thread states, how threads execute concurrently, what surprised you, etc.]

Through this assignment, I gained a deep understanding of how to create and manage threads using the Runnable interface in Java. I learned that multithreading allows a program to execute multiple tasks seemingly simultaneously, thus improving CPU efficiency. I also learned about the thread lifecycle, and how it transitions from the creation state to the execution state and then to the waiting or termination state. It was interesting to see how these threads are controlled using functions like Thread.start() to start the process and Thread.sleep() to simulate execution time. Furthermore, I grasped the importance of scheduling in ensuring fair time allocation among different threads to prevent any one thread from monopolizing the processor. Finally, I realized that precise coordination between these threads is essential for building stable and efficient operating systems.

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

[Describe the specific challenge. Was it understanding the code? Implementing a feature? Using Git? Explain what made it difficult and how it relates to the course concepts.]

The most challenging part for me was implementing the third feature, which involved tracking and calculating the waiting time for each process. The difficulty lay in the need to accurately monitor the time each time a process entered and exited the Ready Queue. I had to use the System.currentTimeMillis() function to calculate the time differences precisely, which required complex programming logic to sum the total time. This challenge is directly related to the course concepts, as it illustrates the complexity of managing context switching in real-world systems. Initially, I encountered calculation errors when re-queuing processes multiple times within the Round-Robin algorithm. However, this challenge helped me understand how to measure scheduler performance and how to handle variables whose values ​​constantly change during route execution.

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
