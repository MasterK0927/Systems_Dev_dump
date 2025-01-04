# What is meant by System Software

- System Software are the softwares that interfaces the Kernel and C library.

- They act as an interface between the user, application software and hardware.

- Eg: GUI, Compiler, Debugger, Webserver and Database

## How it differs from Application Software?

- It uses low level binaries instead of high level binaries.
- It doesn't abstracts much of the OS / hardware details.

## Characteristics

- It can perform low level operations.
- System Calls (`syscalls`).
	- Handles kernel interactions with the system software
	- Around 300 in number
	- 90% of syscalls are supported by different linux dist
- C Library (`libC`).
	- It is a wrapper for syscalls
	- Provides threading support
	- GNU libC is commonly used
- C compiler / linker (`toolchain`).
	- Translates high level language into machine code
	- GCC or GNU C compiler is commonly used

## Components of System Software

1.** Operating System**
- Core of the system software
- Manages hardware, software resources
- Provides services to applications

It encapsulates:

	- **_Kernel_:** It is the lowest level of OS, and it directly interacts with hardware. And generally handles:
		- Process Management using algorithms like round robin, priority scheduling, shortest job first.
		- Memory management using paging, segmentation and virtual memory concepts for allocating memory efficiently.
		- File system management by following the paradigm "Everything is a file".
		- Device Management by providing communication interfacing between OS and peripherals. Those interface are called Device Drivers.
		- Interrupt handling by priotising the tasks and handling the ISRs.

	- **_Shell_:** Acts as an agent between user and kernel. Famous examples are Bash, Zsh or GUI like Explorer, Nautilus


2. **Device Drivers**
- Abstracts the hardware details.
- Enables communication between OS and hardware.
- They operates using protocols such as: 
	- I/O control
	- Interrupts and Polling
	- Memory Mapped I/O
- Graphics Driver interfaces with the GPU to offload rendering tasks.

3. **Utility Programs**
- Auxiliary programs that perform specific tasks to maintain the system's health and performance.
	- Disk Management tools for handling disk partitioning and formatting
	- Backup and Recovery tools for managing data redundancy and restoration
	- Monitoring tools for getting insights into system performanc, resource utilisation and processes. (eg: task manager, htop)


