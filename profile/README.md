High level synthesisable VHDL (hVHDL) is a set of coding patterns for standard VHDL which are designed to greatly increase abstraction level of VHDL source code using standard synthesis tools. The coding patterns are designed to support incremental design, testing and development of the VHDL source code. All code has been tested with an FPGA using Xilinx Vivado, ISE, Lattice Diamond, Intel Quartus or Efinix Efinity tools.

hlVHDL project libraries found in repositories are written to be used as git submodules in any (V)HDL project. To use the submodules, just add them to your project using GiT, add sources to your project compile script, use them for an application, simulate and build. All of the syntesizable code is written in VHDL93, so they should be useable with any tool.

Code in all modules is used through an abstracted interface with subroutines. Code is written using records to specify the registers and a procedure is used to create the logic for the registers as well as accessing the functionality. Most code is thus used with just a signal of module record type and subroutines that then take this signal as argument.

The key idea behind the patterns are 1) all code should be shareable 2) all code should be changeable when needed.
To accomplish these two almost opposite ideas we have designed specific patterns for coding 
   - all functionality should be behind abstract interfaces
   - all code modules should have the possibility to exert backpressure - there should be no need to time code
   - Use any IP from any vendor, add abstract interface if not already given by vendor 
