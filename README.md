# 4-BIT-RIPPLE-COUNTER

 Name: Syed Mohamed Raihan
 
 Ref no: 24900516
 
**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

 Type the program in Quartus software.
 
 Compile and run the program.
 
 Generate the RTL schematic and save the logic diagram.
 
 Create nodes for inputs and outputs to generate the timing diagram.
 
 For different input combinations generate the timing diagram.
 

**PROGRAM**

```
module de12(
    input wire clk,  
    output reg [3:0] count 
); 

always @(posedge clk) 
begin 
    if (count == 4'b1111) 
        
        count <= 4'b0000; 
    else 
        count <= count + 1; 
end 
endmodule
```

 

**RTL LOGIC FOR 4 Bit Ripple Counter**

![Screenshot 2024-12-25 233613](https://github.com/user-attachments/assets/1f8fc9fc-d166-441e-bd15-070ff8e62627)


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![Screenshot 2024-12-25 233640](https://github.com/user-attachments/assets/1360918c-9c9d-4a5f-ad67-bc89c4b6d6d0)

**RESULTS**

Therefore  4 Bit Ripple Counter using verilog is implemented and verified using quartus.
