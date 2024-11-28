# Signal-Handling

Mini assignment in Operating System class to familiarize handling signals in C on Linux.

This program will print its own process id (PID), block SIGUSR1, change the default action of SIGINT (Ctrl+C) to print a custom message with the total number of SIGINT caught, and wait for SIGUSR2 using sigsuspend() along with checking a flag in a loop. After SIGUSR2 is caught and handled, the main program can print a message, restore the oldmask, and terminate.

These were the conditions given in order to change the default command of SIGINT (Ctrl+C).

Then you can test it by pressing Ctrl-C on the same terminal and/or executing the following commands from a different terminal:

kill -SIGINT 12040 

// main program terminal shows a message about SIGINT and the number of occurrences 

kill -SIGUSR1 12040

// main program terminal will show nothing because it blocked this signal 

kill -SIGUSR2 12040

// main program terminal shows a message and terminates the program

These were the commands given in order to test and run the program in order to ensure that the program worked as instructed.
