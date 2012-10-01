POSIXthreads
============

CSE 4733/6733 Homework 2, Fall 2012: Programming with POSIX threads
------------

###1 Objective

  To learn basic multithread programming techniques using POSIX threads and semaphores.
  
###2 Description
You will need to implement the solutions to the producers/consumers problem using POSIX
threads and POSIX semaphores in this homework assignment. The basic algorithms and
solutions to the problems are discussed in detail in our class lectures. You should refer to
your textbook and lecture notes for details.
To aid your implementation, a skeleton code is provided including an implementation of
the FIFO queue data structure, the <code>produce()</code> and <code>consume()</code> functions, and the general
ﬂow of the entire program. You work is to complete the ﬁle pc.c so that it becomes a
complete and correct implementation of the said problem.
Read through the provided code before beginning the remainder of this assignment. Your
primary task in this assignment is to implement the <code>produce()</code>, <code>consume()</code>, and the
main() functions. The function main() accepts from the command-line the total number of
producers and consumers that should be created and then creates them. The producer calls
the produce function to generate a unique integer each time. The integer generated each
time is (id*1000000+offset), where id is the pre-assigned ID of each producer (starting
from 0), offset is the total number of integers generated for a particular producer so far.
In the code, each producer will generate 10 integers and then quit, however, the consumer
will run forever. Thus it is necessary to end the program by manually pressing “Ctrl-C”.