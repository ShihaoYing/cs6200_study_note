Threads case study: PThread
============

***

[toc]

## **Topics**
- PThreads = POSIX Thread
  - POSIX == portable operating system interface
    - POSIX version of Birrell's API
    - specifies syntax and semantics of the operation


## Pthread creation
![P2L3_pthread_creation](pic/P2L3_pthread_creation.png)

### Pthread attributes
```c
int pthread_create(pthread_t *thread,
            const pthread_attr_t *attr,
            void * (*start_routine)(void *),
                void *arg);
```

Pthread_attr_t
- specified in pthread_create
- defines features of the new thread
  - stack size, scheduling policy, priority, inheritance, ***joinable***, system/process scope
- has default behavior with NULL in pthread_create

```c
int pthread_attr_init(pthread_attr_t *attr);
int pthread_attr_destroy(pthread_attr_t *attr);
pthread_attr_{set/get}{attribute}
```

detached & joinable threads
![P2L3_detached_pthread](pic/P2L3_detaching_pthreads.png)