# FIR - Verilog implementation
## Specification
* Data_Width 32
* Tape_Num 11
* Data_Num To be determined by data size
* Interface
  - data_in: stream (Xn)
  - data_out: stream (Yn)
  - coef[Tape_Num-1:0] axilite
  - len: axilite
  - ap_start: axilite
  - ap_done: axilite
* Using one Multiplier and one Adder
* Shift register implemented with SRAM (Shift_RAM, size = 10 DW) – size = 10 DW
* Tap coefficient implemented with SRAM (Tap_RAM = 11 DW) and initialized by axilite write
* Operation
  - ap_start to initiate FIR engine (ap_start valid for one clock cycle)
  - Stream-in Xn. The rate is depending on the FIR processing speed. Use axi-stream valid/ready for flow control
  - Stream out Yn, the output rate depends on FIR processing speed
## Waveform
## 1. Configuration Write
Write Transaction

![image](https://github.com/zeus950068/SOC_Lab/blob/main/soc_lab3_fir/coefficient%20program.png)

Read Transaction

![image](https://github.com/zeus950068/SOC_Lab/blob/main/soc_lab3_fir/Coefficient%20Read%20back.png)

## 2.Configuration Register Address Map
ap_start

![image](https://github.com/zeus950068/SOC_Lab/blob/main/soc_lab3_fir/ap_start.png)

ap_done

![image](https://github.com/zeus950068/SOC_Lab/blob/main/soc_lab3_fir/ap_done.png)


## 3.Streaming Data
Xn stream-in

![image](https://github.com/zeus950068/SOC_Lab/blob/main/soc_lab3_fir/Xn%20stream-in.png)

Yn stream-out

![image](https://github.com/zeus950068/SOC_Lab/blob/main/soc_lab3_fir/Yn%20streaom-out.png)

