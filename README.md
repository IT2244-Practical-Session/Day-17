# Day-17

# 👨‍💻 Process Management in C — Examples using `fork()`, `wait()`, and Shared Memory

This repository contains simple C programs that demonstrate **process creation**, **inter-process communication**, and **process synchronization** using `fork()`, `wait()`, and `sleep()` system calls in Linux.

---

## 📁 Program Summaries

### ✅ 1. `multi_compute.c`
**Description:**
Prompts the user to enter an integer and creates **three child processes**:
- **Child 1**: Computes the factorial.
- **Child 2**: Computes 2 raised to the power of the number.
- **Child 3**: Computes the square of the number.

Each child prints its parent PID. The parent waits for all children to finish.

**Concepts Used:** `fork()`, `getpid()`, `getppid()`, `wait()`

---

### ✅ 2. `sleep_exit.c`
**Description:**
- Prints "Program Started"
- Sleeps for 3 seconds
- Prints "Exiting the program" and exits cleanly

**Concepts Used:** `sleep()`, `exit()`

---

### ✅ 3. `fork_wait.c`
**Description:**
- Parent creates a child process.
- Child prints its PID, sleeps for 2 seconds, and exits with status `0`.
- Parent waits, checks if child exited normally, and prints the exit status.

**Concepts Used:** `fork()`, `sleep()`, `wait()`, `WIFEXITED()`, `WEXITSTATUS()`

---

### ✅ 4. `multi_sleep.c`
**Description:**
- First child sleeps for 1 second.
- Second child sleeps for 3 seconds.
- Parent waits for both and prints a message after they finish.

**Concepts Used:** Multiple `fork()`, `sleep()`, `wait()`

---

### ✅ 5. `shm_writer.c`
**Description:**
Creates a System V shared memory segment and writes user input into it.

**Concepts Used:** `ftok()`, `shmget()`, `shmat()`, `shmdt()`, `IPC_CREAT`

> ⚠️ Note: You will need a matching **reader** program to read from this shared memory segment.

---

## 🧪 Compile & Run

```bash
gcc filename.c -o outputname
./outputname

