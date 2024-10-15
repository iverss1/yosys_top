# yosys_top
A simple project to synthesis RTL to final netlist :blush:, detail process is conducted in [My_CSDN](https://blog.csdn.net/iverss/article/details/142944047?spm=1001.2014.3001.5502 "悬停显示").
## Input
`top.v`
## Output 
 `synth-example.v`
## Process command
`read_verilog top.v`  //Reading the design file using

`synth -top top`  //Mapping to the Internal Library:

`dfflibmap -liberty /path/to/library.lib`  //Mapping Sequential Logic 

`abc -liberty /path/to/library.lib`  //Optimizing the Design

`clean`  //Cleaning Up

`write_verilog top_synth.v`  //Exporting the Netlist
### Ref
【1】[Exploring Logic Synthesis with Yosys: A Tutorial Overview](https://srsapireddy.medium.com/exploring-logic-synthesis-with-yosys-a-tutorial-overview-1d8f63783d86"")

###### The packages provided in this project are for study use only.
