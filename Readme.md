### Overview
This is a fork of Stockfish that has been distributed using MPI to process in parallel across up to 20 computers. The only changes to the codebase to allow for this have been made in UCI.cpp (The command line interface is completely distributed.), thread.cpp (This is where the processing begins) and search.cpp (This is where the processing completes). We've done our best to not modify much of the existing codebase of Stockfish to allow for easy merges from the master branch of Stockfish as it continues in active development.

### Building and Running
Your mileage may vary on Windows. On a Unix system simply use: "make build ARCH=x86-64 COMP=gcc" from the src directory in this repository. The code can then be simulated on a single machine using "/usr/lib64/openmpi/bin/mpirun -n 8 stockfish". This repository also includes code specific to running on the distributed MPac lab at California Polytechnic State University. To do this simply run the included setup.py and then "./labmngr.py -v stockfish". It will run across 20 computers. 

### Using Stockfish
Stockfish is fully supported on our distributed implementation but the best way to see the speed improvements of the distributed version is to run it with a limit on the number of moves explored. This can be done with the following command: "go moves [number here]." We recommend trying the following:
* go moves 100000000
* go moves 1000000000
* go moves 5000000000
* go moves 10000000000

### Comparing Timing
The other branch in this repository ([stockfish-control-master](https://github.com/ethan-kusters/Stockfish/tree/stockfish-control-master)) is the version of Stockfish that was distributed in this branch. It has been slightly modified to match the output of the distributed version and can be used for an apples to apples comparison of the two. 

### Authors
This repository was worked on by Ethan Kusters and Erika Kaplan as a part of CPE 469 (Distributed Systems) at California Polytechnic State University.
