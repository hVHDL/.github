High level synthesisable VHDL (hVHDL) is a set of coding patterns for standard VHDL are designed to greatly increase abstraction level of VHDL source code using standard synthesis tools. The coding patterns are designed to support incremental design, testing and development of the VHDL source code. All code has been tested with an FPGA using Xilinx Vivado, ISE, Intel Quartus or Efinix Efinity tools.

hlVHDL project libraries found in repositories are written to be used as git submodules in any (V)HDL project. To use the submodules, just add them to your project.

Code in all modules is used through an abstracted interface with subroutines. Code is written using records to specify the registers and a procedure is used to create the logic for the registers as well as accessing the functionality. Most code is thus used with just a signal of module record type and subroutines that then take this signal as argument.
