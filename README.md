# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**
This Verilog program implements a 4-bit synchronous down counter.

The counter decreases its value by 1 on every positive edge of the clock (clk).

When the reset (rst) is high, the counter output (out) becomes 0, regardless of the clock.

Since the output is 4-bit wide, it counts down from 15 → 14 → 13 → ... → 0 → 15 → ... in a wrapping sequence.
**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**
Create the Verilog file and type the given code in Quartus.

Compile the design so Quartus generates simulation files.

Open University Program VWF (Waveform Editor).

Add inputs: clk and rst, and add output: out[3:0].

Create a clock signal for clk (e.g., 50% duty cycle).

Apply reset high (1) for a few clock cycles, then make it 0.

Run simulation (RTL/functional simulation).

Observe that:

When rst = 1, output becomes 0000.

When rst = 0, output counts down on every rising clock edge. 

**PROGRAM**
module ex12(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out-1;
end
endmodule

 Developed by:Samantha Shree SV
 RegisterNumber:25017585
*/

**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="1920" height="1080" alt="Screenshot (108)" src="https://github.com/user-attachments/assets/69f2afac-6ee2-4bb7-9b36-a0f71fe38dd4" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="1920" height="1080" alt="Screenshot (109)" src="https://github.com/user-attachments/assets/1656ddff-9ab7-40e3-a0c1-c1ecf5bccb04" />


**RESULTS**
Thus  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables is executed.
