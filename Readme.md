### Overview
This is a fork of Stockfish that has been distributed using MPI to process in parallel across up to 20 computers. The only changes to the codebase to allow for this have been made in UCI.cpp (The command line interface is completely distributed.), thread.cpp (This is where the processing begins) and search.cpp (This is where the processing completes). We've done our best to not modify much of the existing codebase of Stockfish to allow for easy merges from the master branch of Stockfish as it continue in active development.


### Building and Running
Your mileage may vary on Windows. On a Unix system simply use: "make build ARCH=x86-64 COMP=gcc" from the src directory in this repository. The code can then be simulated on a single machine using "/usr/lib64/openmpi/bin/mpirun -n 8 stockfish". This repostiroy also includes code specific to running on the distributed MPac lab at California Polytechnic State University. To do this simply run the included setup.py and then "./labmngr.py -v stockfish". It will run across 20 computers. 


### Authors
This repository was worked on by Ethan Kusters and Erika Kaplan as a part of CPE 469 (Distributed Sytems) at California Polytechnic State University.