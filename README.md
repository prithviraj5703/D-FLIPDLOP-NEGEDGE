# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1.Declare ports for the D flip-flop module, specifying inputs (D, CLK) and outputs (Q, Q_bar).

2.Write Verilog code to create the functionality of the D flip-flop, triggered by the rising edge of the clock signal (posedge CLK).

3.Develop a Verilog testbench to simulate how the D flip-flop responds to different input scenarios.

4.Set up the testbench to test various combinations of input signals (D, CLK) to cover all possible states.

5.Confirm that the D flip-flop's outputs (Q, Q_bar) behave as expected according to its functional table.

6.Ensure that the design doesn't encounter race conditions or undefined states by analyzing the timing and sequence of input changes.

**PROGRAM**
```
 Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:Prithviraj.V RegisterNumber:212222100038
```
```
module DFLIPFLOPNEGEDGE(D,Clock,reset,Q);
input D,reset,Clock;
output reg Q;
always @ (negedge Clock)
if(!reset)
Q <= 0;
else
Q <= D;
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**

![325092384-6787dc73-08fd-4963-aa03-d10a31344514](https://github.com/prithviraj5703/D-FLIPDLOP-NEGEDGE/assets/121418418/1e7f0d54-b67f-41a6-9cb6-57d4ade11428)


**TIMING DIGRAMS FOR FLIP FLOPS**

![325092450-9824c8be-e87d-47c3-bdde-95e699a036b6](https://github.com/prithviraj5703/D-FLIPDLOP-NEGEDGE/assets/121418418/1be582d2-23d8-460a-948c-0be98aace84e)


**RESULTS**

Thus the program to implement a D flipflop using verilog and validating their functionality using their functional tables.
