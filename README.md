# Day-17

👨‍💻 Process Management in C — Examples using fork(), wait(), and Shared Memory
This repository contains simple C programs that demonstrate process creation, inter-process communication, and process synchronization using fork(), wait(), and sleep() system calls in Linux.

📁 Program Summaries
✅ 1. Process Creation and Computation (multi_compute.c)
Description:
Prompts the user for an integer and creates three child processes to perform:

Child 1: Computes the factorial of the number.

Child 2: Calculates 2 raised to the power of the number.

Child 3: Computes the square of the number.

Each child prints its PID and parent PID. The parent waits for all children to complete.

Key Concepts:
fork(), getpid(), getppid(), wait(), arithmetic operations.

✅ 2. Simple Delay (sleep_exit.c)
Description:

Prints a start message.

Sleeps for 3 seconds.

Prints an exit message and exits cleanly using exit(0).

Key Concepts:
sleep(), exit().

✅ 3. Parent Waits for Child (fork_wait.c)
Description:

Parent process creates a child with fork().

Child sleeps for 2 seconds and exits.

Parent waits using wait() and checks child’s exit status.

Key Concepts:
fork(), sleep(), wait(), WIFEXITED(), WEXITSTATUS().

✅ 4. Multiple Children with Sleep (multi_sleep.c)
Description:

First child sleeps for 1 second and exits.

Second child sleeps for 3 seconds and exits.

Parent waits for both children and confirms completion.

Key Concepts:
Multiple fork(), sleep(), wait() for multiple children.

✅ 5. Shared Memory Writer (shm_writer.c)
Description:
Creates a shared memory segment using System V shared memory, writes a user-input string to it.

Key Concepts:
ftok(), shmget(), shmat(), shmdt(), IPC_CREAT.

⚠️ Note: A corresponding reader process would be required to read from the shared memory.

🔧 Compilation and Execution
Use gcc to compile:

bash
Copy
Edit
gcc filename.c -o outputname
./outputname
For example:

bash
Copy
Edit
gcc multi_compute.c -o compute
./compute
📎 Requirements
Linux-based OS

GCC compiler

Basic knowledge of Unix system calls

📚 References

man fork

man wait

man sleep

man shmget

