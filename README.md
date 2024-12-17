# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/user-attachments/assets/2dc72d2b-31f7-4664-80f7-eb41f3801975)
 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/user-attachments/assets/a46bf549-3f48-4546-9a0e-d5343537b463)
 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/user-attachments/assets/020c136d-2d4a-4dc6-b1d6-c01aec761ff3)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/user-attachments/assets/cdabeea3-964e-49db-9f68-0d9327ce1af2)
 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by:Paveen Kumaran SV
RegisterNumber:24000025

module sr_flipflop(s,r,clk,q,qbar);

input s,r,clk;

output reg q;

output reg qbar;

initial

begin

q=0;

qbar=1;

end

always @(posedge clk)

begin

q=s|(~r&q);

qbar=r|(~s&~q);

end

endmodule

**RTL LOGIC FOR FLIPFLOPS**

![image](https://github.com/user-attachments/assets/39b4f8bc-404d-4958-b5a2-de525eff8d73)

**TIMING DIGRAMS FOR FLIP FLOPS**

**RESULTS**
Thus the truth table of sr_flipflop in Quartus || using Verilog programming are studied, verified and executed successfully.
