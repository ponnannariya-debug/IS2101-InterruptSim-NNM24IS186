# Interrupt Handler Simulation

# Description
This project is a small simulation of how interrupt handling works in a computer system.
It demonstrates how different devices such as the keyboard, mouse, and printer send interrupt requests to the CPU.
The CPU then decides which interrupt to handle first based on priority.
Each device has a fixed priority level:
Keyboard → High priority
Mouse → Medium priority
Printer → Low priority
Masking is also included, which means some devices can be temporarily ignored during the execution.
This simulation helps visualize how interrupts are managed in real systems using basic C programming and pthreads.

# Features
Multit Threading using pthreads
Priority-based interrupt handling (Keyboard > Mouse > Printer)
Masking support to ignore certain interrupts
Displays clear and readable output
Ends with a summary after all interrupts are handled

# How to Compile and Run
gcc interrupt_sim.c -o interrupt_sim -lpthread
interrupt_sim

# Input and Output
Input:
No manual input is needed.
Interrupts are generated randomly by the program.
Sample Output:
=== INTERRUPT HANDLER SIMULATION ===
Priority: Keyboard > Mouse > Printer

Keyboard Interrupt Received -> Processing ISR -> Done
Interrupt Ignored (Masked Device)
Printer Interrupt Received -> Processing ISR -> Done
Keyboard Interrupt Received -> Processing ISR -> Done
Interrupt Ignored (Masked Device)
Printer Interrupt Received -> Processing ISR -> Done

All interrupts handled successfully. Execution complete.

Output:

<img width="757" height="323" alt="Screenshot 2025-10-31 094134" src="https://github.com/user-attachments/assets/06fb7be5-8b06-4d9b-b7c0-741cff75a9c6" />



#  Conclusion
This simulation helped in understanding how interrupt handling works in real computer systems.
It shows how priorities and masking control which device is attended first by the CPU.
Using threads and mutex locks makes the handling process safe and synchronized.
Overall, it provides a simple and clear way to learn interrupt management and multitasking in operating systems.
