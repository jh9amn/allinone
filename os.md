## 1. What is the main purpose of an Operating System? Discuss different types.

### What is an Operating System?

An **Operating System (OS)** is system software that acts as an interface between the **user/application programs and computer hardware**.

### Main purposes of an OS

1. **Resource Management**
   Manages CPU, memory, storage, and I/O devices.

2. **Process Management**
   Creates, schedules, and terminates processes and allocates CPU time to them.

3. **Memory Management**
   Allocates and deallocates memory to processes and manages virtual memory.

4. **File Management**
   Creates, reads, writes, deletes, and organizes files and directories.

5. **Device Management**
   Manages hardware devices such as keyboards, disks, printers, and network devices using device drivers.

6. **Security and Protection**
   Controls access to system resources and protects processes and data.

7. **User Interface**
   Provides interfaces such as CLI and GUI for users to interact with the system.

### Types of Operating Systems

#### 1. Batch Operating System

* Jobs are collected and executed in batches without direct user interaction.
* Suitable for large, repetitive jobs.
* Example: Early mainframe systems.

#### 2. Time-Sharing Operating System

* CPU time is divided into small time slices and shared among multiple users/processes.
* Provides interactive response.
* Example: Unix/Linux systems.

#### 3. Multiprogramming Operating System

* Keeps multiple programs in memory at the same time.
* CPU switches to another program when one is waiting for I/O.
* Improves CPU utilization.

#### 4. Multitasking Operating System

* Allows multiple tasks/processes to run seemingly at the same time.
* Example: Windows, Linux, macOS.

#### 5. Multiprocessing Operating System

* Uses multiple CPUs or CPU cores to execute processes in parallel.
* Improves performance and reliability.

#### 6. Real-Time Operating System (RTOS)

* Provides a predictable response within a specified time limit.
* Used where timing is critical.
* Examples: FreeRTOS, VxWorks.

#### 7. Distributed Operating System

* Manages multiple connected computers and makes them appear like a single system to users.
* Focuses on resource sharing and coordination.

#### 8. Network Operating System

* Provides services for managing computers connected through a network.
* Examples: Windows Server, Linux Server.

### Interview Short Answer

> An Operating System is system software that acts as an interface between applications/users and hardware. Its main purpose is to manage resources such as CPU, memory, storage, files, and I/O devices while providing security and a convenient interface to users. Common types include Batch, Time-Sharing, Multiprogramming, Multitasking, Multiprocessing, Real-Time, Distributed, and Network Operating Systems.

---

# 2. What is a Socket, Kernel, and Monolithic Kernel?

## Socket

A **socket** is an endpoint used for communication between two processes, usually over a network.

A socket is commonly identified by:

* **IP address**
* **Port number**
* **Protocol** such as TCP or UDP

For example:

```text
192.168.1.10 : 8080
     IP          Port
```

A server creates a socket, binds it to an IP/port, listens for connections, and accepts client connections.

### Interview Short Answer

> A socket is a communication endpoint that allows processes to communicate with each other, either on the same machine or across a network. It is commonly associated with an IP address, port number, and communication protocol.

---

## Kernel

The **kernel** is the core component of an operating system. It runs in a privileged mode and directly manages hardware resources.

Main responsibilities:

* Process management
* Memory management
* Device management
* File-system management
* Networking
* System calls

For example:

```text
Application
     |
 System Calls
     |
   Kernel
     |
 Hardware
```

Applications normally cannot directly access hardware. They request services from the kernel through **system calls**.

### Interview Short Answer

> The kernel is the core part of an operating system that manages hardware resources and provides essential services to applications through system calls.

---

## Monolithic Kernel

A **monolithic kernel** is a kernel architecture where most major OS services run inside the **kernel space**.

These services can include:

* Process management
* Memory management
* File systems
* Device drivers
* Networking

```text
        User Space
    Applications
          |
     System Calls
          |
        Kernel Space
   -------------------
   Process Management
   Memory Management
   File System
   Device Drivers
   Networking
   -------------------
          |
       Hardware
```

### Advantages

* High performance because components communicate directly within kernel space.
* Efficient communication between OS components.

### Disadvantages

* A bug in one kernel component can potentially affect the entire system.
* The kernel can become large and complex.

### Example

**Linux** is generally considered a **monolithic kernel**, although it supports dynamically loadable kernel modules.

### Interview Short Answer

> A monolithic kernel is a kernel architecture where major operating system services such as process management, memory management, file systems, device drivers, and networking run in kernel space. It generally provides high performance but can have a larger and more complex kernel. Linux is an example.
