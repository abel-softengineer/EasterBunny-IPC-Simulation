🐰 Easter Bunny OS Simulation – IPC & Process Management

This project is a Linux-based system simulation written in C. It demonstrates low-level operating system concepts such as process synchronization, parent-child process forking, and Inter-Process Communication (IPC) using pipes. The project was developed as part of the Operating Systems course at ELTE.
🛠️ Technical Deep Dive

The application models a competition where a "Master Bunny" (parent process) coordinates several "Rabbit" contestants (child processes) through a complex lifecycle:

    Process Architecture: Utilizes fork() to create concurrent child processes for each contestant, ensuring parallel task execution.

    Inter-Process Communication (IPC): Implements anonymous pipes to stream data (randomly generated scores) from child processes back to the parent for aggregation.

    Robust Data Parsing: Features a custom-built parser using strtok to handle file I/O from a pipe-delimited (|) text database (nyuszik.txt).

    System Resource Management: Ensures clean execution by managing file descriptors (close) and synchronizing process termination using waitpid to prevent zombie processes.

🚀 How to Run

    Compile the source code using gcc:
    Bash

    gcc -o bunny_sim nyuszi.c

    Execute the binary:
    Bash

    ./bunny_sim

📂 Project Structure

    main.c: The core logic including the CLI menu, file operations, and the simulation loop.

    nyuszik.txt: A persistent text-based database storing participant names, poems, and scores.

    storage.php / data.php (for the previous project): Demonstrates architectural consistency across different languages.
