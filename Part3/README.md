# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is multiple tasks happening at the same time. This refers to simplify the programming.
 Paralellism is using multiple processing units to do multiple operations at the same time. Here the goal is to make a faster program, unlike concurrency which seeks to make programming easier. 
 
 ### Why have machines become increasingly multicore in the past decade?
 > Since CPU's are close to the physical limits of their clock speed, we instead add more cores.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > It helps in solving problems where multiple tasks are solved at the same time. E.g in the elevator project, we will have multiple elevators moving, each could been seen as it's own task (simplified).
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > It makes it easier since we can run multiple tasks at the same time, but at the same time it can make the code more complex.
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Processes run on the seperate memory spaces.
 Threads run on the same memory space.
 Green threads are emulated threads by a runtime library or virtual machine on OS that does not support threading.
 Coroutines are processes that mostly run like threads but share a few global variables with eachother.
 
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > Thread
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > It prevents multiple threads from executing bytecode at the same time. This removes a lot of the potential advantage of multicore systems. 
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Code a lot outside of GIL, in a seperate module.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > The GOMAXPROCS variable limits the number of operating system threads that can execute user-level Go code simultaneously. The n is that number.
