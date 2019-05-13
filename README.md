# Pipe_SPIM
This Project modifies the source code of SPIM simulator so that it can handle pipelining

* SPIM is a MIPS processor simulator, designed to run assembly language code for this architecture. Although the MIPS architecture is designed to support the pipelining, the current version of SPIM does not support the pipelining. In this project, the source code of SPIM is modified so that it can output the correct number of cycles needed to complete assembly instructions in a pipelined technique.


* Notes:
- 5-stage pipeline is used (IF, ID, EX, MEM, and WB).
- No cache miss assumption.
- Arithmetic and logical instructions determine the value of destination register in the EX stage.
- Load and store instructions determine the value of destination register in the MEM stage.
- The decision of branch (direction/target) and jump (target address) are determined in the ID stage.
- 'static not-taken' policy for branch prediction is used.
- The pipeline detectd data and control hazards and calculated the required execution cycles considering the forwarding and pipeline stalls.
- The cycles consumed before entering the main function are not counted.

* Check the image (Building_Spim.jpg) for details on "How to Build SPIM"




* How to run?
- Download SPIM using:
$ wget http://www.cs.wisc.edu/~larus/SPIM/spim.tar.gz

- Replace the run.c in CPU directory with my run.c

- The current code of mine only supports input as an assembly code in MIPS. To run it please use the following command:

$ ./spim -file [filename]

