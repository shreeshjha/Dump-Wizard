# Ram Dump Collection Tool

### Dump-Wizard
This program creates a memory dump of the current process and writes it to a file. It does this by iterating over the virtual memory regions of the process using the VirtualQuery function, and for each region that is committed and readable, it allocates a buffer, reads the memory into the buffer using the ReadProcessMemory function, and writes the buffer to a file using the WriteFile function. Additionally, the program writes the contents of the memory dump to a text file, along with the address and size of each memory region.

### Dump-Analyzer
This program analyzes a memory dump file generated from Dump-Wizard and writes the analysis to a text file. It uses the Windows API to open the memory dump file, allocate memory to read it into, and then read the contents of the file into memory. The program then analyzes the memory dump, writing the results to a text file. The output includes the dump file name, the file size, and the contents of the file, represented as 8-digit hexadecimal values. The program is designed to run on Windows operating systems and requires the Microsoft Visual C++ compiler to build.
