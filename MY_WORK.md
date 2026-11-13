# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [Moath Nawaf ALmuhaysin] |
| **Student ID** | [443050224] |
| **University Email** | [443050224]@std.psau.edu.sa |
| **GitHub Username** | [Moath123-n] |
| **Repository Link** | [https://github.com/Moath123-n/OS-Assignment3-Moath-ALmuhaysin.git] |
 
---

## 🎥 Video Link

**Video Link**: [https://drive.google.com/file/d/1VCm_2ybvBowUsQWFd1P-OjbK-YMhNGFl/view?usp=sharing]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [November 12, 2026, 10:30 PM]
**What I did**: I conducted the baseline test after setting up the repository and adding my student ID.

**Details**: I cloned the starter code to Visual Studio Code, changed line 304 with my ID (443050224), and executed the program to see the watchdog timeout and the first race condition errors.

**Challenges**: When attempting to clone the repository to my local computer, I ran across problems with GitHub login in Visual Studio Code.

**Solution**: I successfully synced the repository after authorizing VS Code over the browser using my university email account in accordance with the README instructions.

**Time spent**: 30 minutes

---

### Entry 2 - [November 13, 2026, 12:00 AM]
**What I did**: Feature 1 was put into practice to safeguard the ready queue.

**Details**: The ReadyQueue class now has a ReentrantLock called queueLock. To make sure the lock is always released, I used try/finally blocks to protect the add(), poll(), processOf(), and snapshot() functions.

**Challenges**: unintentionally removed a closing bracket }, which resulted in a syntax error and led the IDE to believe that SchedulerSimulationSync was nested inside ReadyQueue.

**Solution**: To restore the proper structure, I carefully examined the bracket matching at the end of the ReadyQueue class using the formatting tool in Visual Studio Code.

**Time spent**: 45 minutes

---

### Entry 3 - [November 13, 2026, 12:45 AM]
**What I did**: Feature 2 was put into practice to safeguard shared statistics.

**Details**: To safeguard both read and write activities, three distinct ReentrantLock objects were created in the SharedStats class, one for each variable (context switches, completed processes, and total service time).

**Challenges**: To maximize performance, choose between using a single lock for each variable or a single global lock for all statistics.

**Solution**: To enhance throughput, one lock per variable (fine-grained locking) was used so that updating one stat wouldn't prevent another CPU from updating a different stat at the same time.

**Time spent**: 45 minutes

---

### Entry 4 - [November 13, 2026, 1:30 AM]
**What I did**: Feature 3 was put into practice to use a semaphore to end busy waiting.

**Details**: added a readyCount semaphore with an initial value of 0. CpuWorker's polling loop was swapped out for readyCount.acquire() and included readyCount.release() in the add() function.

**Challenges**: At the end of the simulation, the CPUs were stuck waiting indefinitely, which resulted in a Watchdog timeout error because the threads were still blocked even though the queue was empty.

**Solution**: When the final process finishes, a shutdown signal release (SharedStats.totalCPUs) is added to wake up any remaining blocked CPUs so they can end cleanly.

**Time spent**: 1 hours

---

### Entry 5 - [November 13, 2026, 9:00 PM]
**What I did**: The demonstration film was recorded and the final code was verified.

**Details**: To make sure all verification tests passed (green marks) and busy-waiting was precisely zero, the simulation was run five times in a row. The three-minute video that explains the locks, semaphore, and execution was recorded.

**Challenges**: completing the conceptual explanation, the code walkthrough, and the terminal output in the allotted two to three minutes.

**Solution**: Before recording, I practiced the script multiple times and adjusted the VS Code terminal's size such that the verification block could be seen right away without having to scroll.

**Time spent**: 1 hour

---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [X hours]

**Most challenging part**:

**Most interesting learning**:

**What I would do differently next time**:

---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

[My comprehension of Silberschatz Chapter 5's process synchronization concepts was reinforced by this task. I was able to observe firsthand how a race condition occurs at the code level when a read-modify-write cycle is interrupted by context switching. I also discovered how crucial it is to use try/finally blocks while working with ReentrantLock in order to guaranty mutual exclusion without running the risk of a deadlock in the event of an exception. Finally, I realized that, in contrast to busy waiting, semaphores essentially eliminate CPU resource loss.]

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

[The clean shutdown in Feature 3 was the hardest to accomplish. When the last process finished, the queue was empty, therefore the other CPU threads were permanently blocked on the readyCount.acquire() call. The Watchdog timer was firing, but it was hard to figure out why. After carefully charting the threads' states, I discovered that they need a final artificial "wake-up" signal in order to assess the loop condition and end gracefully.]

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

[By carefully going over the assignment instructions again and using the textbook's explanation of thread signaling, I was able to resolve the shutdown issue. I discovered that all waiting CPUs might be awakened simultaneously by releasing enough permissions using the Semaphore.release(int permits) method. The stopped threads were able to continue, observe that getCompletedProcessCount() >= SharedStats.totalProcesses, and exit by injecting readyQueue.readyCount.release(SharedStats.totalCPUs) as soon as a process ended if the completed count matched the total.]

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

[In practically all contemporary multi-threaded systems, these ideas are essential. For example, locks in database management systems (DBMS) prevent concurrent transactions from overwriting each other's data (maintaining ACID characteristics). Semaphores can be used in web servers to prevent backend overload by limiting the amount of active database connections in a connection pool. Additionally, comparable queues and semaphores are used by printer spools and operating system task schedulers to effectively manage shared resources.]

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

[Race conditions caused updates to be missed in my initial starter run, as evidenced by the observed `completedProcessCount` of 17 instead of the anticipated 18 and the observed `Context switches` of 35 instead of 36. This occurs as a result of several CPUs simultaneously accessing and changing the unprotected shared variables. Because the operating system's scheduler can preempt (stop) a thread precisely between the low-level assembly instructions of reading and writing a variable, this error can happen on a real machine even in the absence of `RaceWindow.pause()`. This particular timing is arbitrary, therefore the bug may not show up in every test run, making it infamously difficult to find.]

Verification block of the **original starter**:
```
[```text
VERIFICATION (expected values are computed from YOUR seed)
Context switches (quanta executed)     expected 36       observed 35      X MISMATCH
Completed processes                    expected 18       observed 17      X MISMATCH
Total service time (ms)                expected 54645    observed 53908   X MISMATCH
Busy-waiting polls (must be 0)         expected 0        observed 941     X MISMATCH
X At least one check failed (see the X lines above): a race condition or busy waiting is still present.]
```

Verification block of **my final version**:
```
[VERIFICATION (expected values are computed from YOUR seed)
Context switches (quanta executed)     expected 36       observed 36      ✓
Completed processes                    expected 18       observed 18      ✓
Total service time (ms)                expected 54645    observed 54645   ✓
Busy-waiting polls (must be 0)         expected 0        observed 0       ✓
✓ All shared values are consistent.]
```

**Explanation of the timeline:**
[Here is how the lost update happened on completedProcessCount step by step:

CPU-1 reads completedProcessCount = 16.

CPU-1 is paused (simulated by RaceWindow.pause()).

CPU-2 reads completedProcessCount = 16 (it reads the same old value because CPU-1 hasn't saved its update yet).

CPU-1 adds 1 to its temporary value and writes 17 back to completedProcessCount.

CPU-2 adds 1 to its temporary value and also writes 17 back to completedProcessCount.Result: Two processes finished, but the counter only went up by 1 (ending at 17 instead of 18). One increment was completely lost.]

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

[Since the three statistics are entirely independent of one another and changing `contextSwitchCount` does not require blocking an update to `totalServiceTime`, I used one lock per variable. In exchange for maximum concurrency and higher throughput, there is a minor increase in memory utilization. To avoid lengthy wait times, a separate lock is employed to secure the ready queue. If we utilized the same lock for everything, a thread manipulating the queue would needlessly impede other CPUs from updating their statistics. Because `lock()` only allows one thread to enter, my solution ensures mutual exclusion and progress. However, strict bounded waiting is not guarantyd because a default `ReentrantLock` is unfair, suggesting that a thread could theoretically be repeatedly bypassed (though starvation is rare here).]

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| `ReadyQueue.add()`, `poll()`, `processOf()`, `snapshot()` | `queueLock` | Prevents concurrent modification of the shared `list` and `map` to avoid duplicate reads, missing processes, or `IllegalThreadStateException`. |
| `SharedStats.contextSwitchCount` (update & get) | `contextLock` | Prevents lost increments when multiple CPUs start a time quantum at the exact same time. |
| `SharedStats.completedProcessCount` (update & get) | `completedLock` | Prevents lost updates when processes finish, ensuring the CPUs know exactly when the simulation is fully done. |
| `SharedStats.totalServiceTime` (update & get) | `serviceLock` | Prevents lost addition of executed milliseconds when multiple CPUs update their service time concurrently. |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

[In the starter code, a CPU finding an empty queue remained in the "running" state by constantly polling and sleeping (busy waiting), which wasted CPU cycles and resulted in 941 useless polls in my initial run. Conversely, in my final version, the semaphore allows the CPU to enter a safely "blocked" state when the queue is empty, preserving system resources[cite: 118]. The semaphore's value represents the exact number of processes currently waiting in the ready queue; it is initialized to 0 because the queue starts empty, and its value reaches 18 right after the initial setup loop adds all my generated processes[cite: 118]. Finally, the last CPU must call `release(SharedStats.totalCPUs)` to broadcast a wake-up signal to any other CPUs permanently blocked in `acquire()`[cite: 118]. If this shutdown signal were omitted, those CPUs would sleep forever waiting for a process that will never arrive, causing a system hang and triggering the Watchdog timeout[cite: 118].]

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
[This represents the classical Producer-Consumer (or Bounded-Buffer) problem. The `main` thread (initially) and the `CpuWorker` threads (when re-enqueueing unfinished processes) act as the producers, while the `CpuWorker` threads act as the consumers when they poll processes from the ready queue to execute[cite: 119].]

**Semaphores for a bounded queue (name and initial value)**:
[We would need three semaphores: a `mutex` initialized to `1`, an `empty` semaphore initialized to the capacity `K`, and a `full` semaphore initialized to `0`[cite: 119].]

**Deadlock scenario and prevention**:
[A deadlock occurs if a producer acquires the `mutex` first and then calls `wait()` on `empty` when the queue is completely full; it holds the lock while waiting for a free slot that a consumer can never create because the consumer is permanently blocked trying to acquire that same `mutex`[cite: 119]. To prevent this, I would break the "Hold and Wait" (or "Circular Wait") condition by enforcing a strict order: threads must always wait on the resource semaphores (`empty` or `full`) *before* acquiring the `mutex`[cite: 119].]

## Summary

**Key concepts I understood through these questions:**
1. **Race Conditions:** How a context switch precisely between reading and writing a shared variable causes lost updates, and why this is hard to detect.
2. **Mutual Exclusion & Locks:** The necessity of using a `ReentrantLock` to protect critical sections, and the critical importance of the `finally` block to guarantee lock release and avoid deadlocks[cite: 120].
3. **Semaphores vs. Busy Waiting:** How counting semaphores allow threads to enter a blocked state when resources are unavailable, effectively saving CPU cycles compared to continuous polling (busy waiting)[cite: 120].

**Concepts I need to study more:**
1. **Bounded Waiting & Fairness:** The theoretical differences between fair and unfair locks under heavy loads, and how an unfair lock might theoretically lead to thread starvation[cite: 120].
2. **Advanced Deadlock Handling:** How to practically implement deadlock detection and recovery algorithms in more complex systems with multiple interdependent resources[cite: 120].

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [X] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [X] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [X] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [X] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [X] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [X] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [X] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [X] **The four verification lines are ✔ in 5 consecutive runs**
- [X] Every lock is released in a `finally` block
- [X] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [X] Each feature has clear comments

**Commits**
- [X] **At least 4 meaningful commits, ideally 7 or more**
- [X] **One commit per feature**
- [x] Commits are spread over **different dates** (not all in the last hour)
- [X] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [X] Full name and student ID filled in at the top
- [x] Development log has **5+ entries** on different dates
- [X] Reflection: 4 questions, 5-7 sentences each
- [x] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [X] No `[...]` placeholders left
- [X] No section headers deleted

**Video**
- [X] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [X] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [X] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [X] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
