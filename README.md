# BitTwiddler
A bit of bit twiddling fun in C from CS 367 

### Specs

unix> tar xvf 1_datalab-handout.tar

This will cause a number of files to be unpacked in the directory. The only file you will be modifying and
turning in is bits.c.

The bits.c file contains a skeleton for each of the programming puzzles. Your assignment is to complete
each function skeleton using only straightline code for the integer puzzles (i.e., no loops or conditionals)
and a limited number of C arithmetic and logical operators. Specifically, you are only allowed to use the
following eight operators:

! ˜ & ˆ | + << >>

Included some autograding tools in the handout directory — btest, dlc, and driver.pl — to help you check the correctness of your work.

* btest: This program checks the functional correctness of the functions in bits.c. To build and use it, type the following two commands:

unix> make unix> ./btest

Notice that you must rebuild btest each time you modify your bits.c file.

You’ll find it helpful to work through the functions one at a time, testing each one as you go. You can use the -f flag to instruct btest to test only a single function:

unix> ./btest -f bitAnd

You can feed it specific function arguments using the option flags -1, -2, and -3:
unix> ./btest -f bitAnd -1 7 -2 0xf
Check the file README for documentation on running the btest program.
* dlc: This is a modified version of an ANSI C compiler from the MIT CILK group that you can use
to check for compliance with the coding rules for each puzzle. The typical usage is:
unix> ./dlc bits.c


The program runs silently unless it detects a problem, such as an illegal operator, too many operators,
or non-straightline code in the integer puzzles. Running with the -e switch:
unix> ./dlc -e bits.c
causes dlc to print counts of the number of operators used by each function. Type ./dlc -help
for a list of command line options.
* driver.pl: This is a driver program that uses btest and dlc to compute the correctness and
performance points for your solution. It takes no arguments:
unix> ./driver.pl




