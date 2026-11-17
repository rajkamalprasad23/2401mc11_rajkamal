Rajkamal Prasad
2401mc11

question 1 - counting semaphores

Added a new file synctest for implementing counting semaphores in xv6.  Created a table of 8 semaphores with their value and in-use status, protected using spinlock.Added three system calls sem_init(), sem_wait() and sem_post() for using the semaphores from user programs.Updated the required kernel and user files like syscall.c, sysproc.c, user.h, usys.S and Makefile.Created synctest.c to test synchronization between three child processes, so they print A B C in proper order.

question 2 - free pages and virtual to physical address

Changed kalloc.c to maintain the count of free physical memory pages. The counter is increased when a page is freed using kfree() and decreased when a page is allocated using kalloc(). added freepages() system call to get the current number of free pages. added address translation function using va2pa() which converts a user virtual address into its physical address and returns -1 for invalid addresses. created memtest.c to check free pages, address translation and the difference in parent and child physical addresses after fork.


