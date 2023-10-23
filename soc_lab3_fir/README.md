# FIR - Verilog implementation
## Specification
* Data_Width 32
* Tape_Num 11
* Data_Num To be determined by data size
## Interface
* data_in: stream (Xn)
* data_out: stream (Yn)
* coef[Tape_Num-1:0] axilite
* len: axilite
* ap_start: axilite
* ap_done: axilite
* Using one Multiplier and one Adder
* 
