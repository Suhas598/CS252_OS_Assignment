Q3.21

Here, the child process will output the sequence of numbers obtained from the algorithm as specified under the conditions of the Collatz conjecture.
Here, the parent and child processes have their own copies of the data.

The fork() system call creates a child process, and returns process ID. Both the parent and child processes run concurrently after this line. 
The fork() system call always returns 0 to the newly created process, i.e the child process is assigned a pid = 0
and the process ID to the parent process (a non-negative integer).

The parent process executes first, whose process ID is non zero, and hence, the code enters the else block. Here, the wait() function is called, and so, the parent process waits until the child process completes execution, that is, returns a value (in this case, 0).

The child process executes, whose process ID is zero, and hence, the code enters the if (pid==0) block. 
Here, the algorithm for the Collatz conjecture is executed.

After child process is done, process ID resumes execution and the program is completed. 
