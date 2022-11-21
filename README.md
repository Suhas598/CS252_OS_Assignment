# CS252_OS_Assignment

The assignment consists of two questions from the exercise section of the 10th edition of Operating System Concepts by Abraham Silberschatz, Peter Baer Galvin and Greg Gagne.

# Questions
## Question 1: Chapter 3 - 3.21

The Collatz conjecture concerns what happens when we take any positive integer n and apply the following algorithm:
n = { n∕2, if n is even
     3 × n + 1, if n is odd

The conjecture states that when this algorithm is continually applied,
all positive integers will eventually reach 1. For example, if n = 35, the
sequence is
35, 106, 53, 160, 80, 40, 20, 10, 5, 16, 8, 4, 2, 1

Write a C program using the fork() system call that generates this sequence in the child process. The starting number will be provided from the command line. For example, if 8 is passed as a parameter on the command line, the child process will output 8, 4, 2, 1. Because the parent and child processes have their own copies of the data, it will be necessary for the child to output the sequence. Have the parent invoke the wait() call to wait for the child process to complete before exiting the program. Perform necessary error checking to ensure that a positive integer is passed on the command line.

## Question 2: Chapter 4- 4.24

An interesting way of calculating π is to use a technique known as Monte Carlo, which involves randomization. This technique works as follows: Suppose you have a circle inscribed within a square, as shown in Figure 4.25. (Assume that the radius of this circle is 1.)

• First, generate a series of random points as simple (x, y) coordinates. These points must fall within the Cartesian coordinates that bound the square. Of the total number of random points that are generated, some will occur within the circle.

• Next, estimate π by performing the following calculation:

π = 4× (number of points in circle) / (total number of points)

Write a multithreaded version of this algorithm that creates a separate thread to generate a number of random points. The thread will count the number of points that occur within the circle and store that result in a global variable. When this thread has exited, the parent thread will calculate and output the estimated value of π.

It is worth experimenting with the number of random points generated. As a general rule, the greater the number of points, the closer the approximation to π.

In the source-code download for this text, you will find a sample program that provides a technique for generating random numbers, as well as determining if the random (x, y) point occurs within the circle.

Readers interested in the details of the Monte Carlo method for estimating π should consult the bibliography at the end of this chapter. In Chapter 6, we modify this exercise using relevant material from that chapter.
