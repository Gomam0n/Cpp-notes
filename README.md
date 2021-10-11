# Cpp-notes
notes of C++
# baguwen
## Difference between TCP(Transmission Control Protocol) and UDP(User Datagram Protocol)
1. TCP requires an established connection to transmit data while UDP is a connectionless protocol with no requirements for opening, maintaining, or terminating a connection.
2. TCP is **reliable** as it guarantees the delivery of data to the destination router. The delivery of data to the destination cannot be guaranteed in UDP.
3. TCP is comparatively slower than UDP. UDP is faster, simpler, and more efficient than TCP.
4. TCP doesn’t support Broadcasting. UDP supports Broadcasting.
5. TCP has a (20-60) bytes variable length header. UDP has an 8 bytes fixed-length header.
6. TCP is used by HTTP, HTTPs, FTP, SMTP and Telnet. UDP is used by video conferencing, streaming, DNS, VoIP, etc

## Difference between thread and process
1. A process is a program under execution. Thread means segment of a process.(A thread is a lightweight process that can be managed independently by a scheduler.)
2. Processes are totally independent and don’t share memory. A thread may share some memory with its peer threads.
3. Processes require more time for creation and termination. Threads require less time for creation.
4. Process consume more resources. Thread consume less resources.
5. Process switching uses interface in operating system. Thread switching does not require to call a operating system and cause an interrupt to the kernel.

## IPC
1. Pipes
2. Names Pipes
3. Message Queuing
4. Semaphores
5. Shared memory
6. Sockets

## Difference between stack and heap
1. Stack is allocated automatically by compiler and has a fixed size. Heap is manually allocated by the programmer and can be resized.
2. Stack memory is allocated in a contiguous block. Heap is in a hierarchical data structure.
3. The access to stack is fast and cost less while the access to heap is slow and cost more.
4. The memory of stack grows downwards while the memory of heap grows upwards.

## Inline function
C++ provides an inline functions to reduce the function call overhead. Inline function is a function that is expanded in line when it is called. When the inline function is called whole code of the inline function gets inserted or substituted at the point of inline function call. This substitution is performed by the C++ compiler at compile time. Inline function may increase efficiency if it is small.  
Advantages:
1. Function call overhead doesn’t occur.
2. It also saves the overhead of push/pop variables on the stack when function is called.
3. It also saves overhead of a return call from a function.
4. When you inline a function, you may enable compiler to perform context specific optimization on the body of function. Such optimizations are not possible for normal function calls. Other optimizations can be obtained by considering the flows of calling context and the called context.
5. Inline function may be useful (if it is small) for embedded systems because inline can yield less code than the function call preamble and return.  
Disadvantages:
1. The added variables from the inlined function consumes additional registers, After in-lining function if variables number which are going to use register increases than they may create overhead on register variable resource utilization. This means that when inline function body is substituted at the point of function call, total number of variables used by the function also gets inserted. So the number of register going to be used for the variables will also get increased. So if after function inlining variable numbers increase drastically then it would surely cause an overhead on register utilization.
2. If you use too many inline functions then the size of the binary executable file will be large, because of the duplication of same code.
3. Too much inlining can also reduce your instruction cache hit rate, thus reducing the speed of instruction fetch from that of cache memory to that of primary memory.
4. Inline function may increase compile time overhead if someone changes the code inside the inline function then all the calling location has to be recompiled because compiler would require to replace all the code once again to reflect the changes, otherwise it will continue with old functionality.
5. Inline functions may not be useful for many embedded systems. Because in embedded systems code size is more important than speed.
6. Inline functions might cause thrashing because inlining might increase size of the binary executable file. Thrashing in memory causes performance of computer to degrade.
##	C++ vs Go
1.	C++ is an object-oriented programming language. Go is a procedural and concurrent programming language
2.	The code of Go is simpler and more compact
3.	There is automatic garbage collector in Go.
4.	Both have pointers. But Go does not allow pointer arithmetic. 
5.	Go has a strict requirement of the format of the codes.
##	C++ vs Python
1.	Python runs through interpreter while C++ is pre-compiled
2.	There is automatic garbage collector in Python.
