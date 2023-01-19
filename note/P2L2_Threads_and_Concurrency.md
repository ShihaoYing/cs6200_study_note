Threads and Concurrency 
============

***

[toc]

## **Topics**
- What are threads?
- How threads different from processes?
- What data structures are used to implement and manage threads?

## Definition:
A thread  is like a worker in a toy shop.
![thread_definition](pic/P2L2_thread_definition.png)

## Process vs Thread

- Thread will share the same code, data, and files.
- Each thread will need to have a different program counter, stack pointer, stack, thread-specific registers.
  - For each and every thread, we will have to have separate data structures to represent this pre-thread information.

![thread_vs_process](pic/P2L2_thread_vs_process.png)

### Benefits of Multithreading
- parallelization ==> Speed up 
- specialization ==> hot cache!