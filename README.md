# TITTLE
To Design and simulate mod 5 synchronous up counter with JK flip flop using Verilog

# THEORY

Mod 7 synchronous counter
A mod 7 counter counts from 0 to 6.
The number of flip-flops required to design a mod 7 counter can be calculated using the formula 2" >=
N, where n is equal to no of flip-flop and N is the mod number. In this case, the possible value on n
which satisfies the equation. Hence, the required number of flip-flops is 3.
The type of flip flop required to design the counter is JK flip- Bop
We can draw the state diagram for mod 7 counter descubing the state flow in current and next state
Using the excitation table of JK flip-flop, we need to obtain the flip-flop inputs for each state that we
obtained in the third step
Making K Map for each input combination and simplifying it to get the minimized Boolean expression.
Using the Boolean expressions obtained in step 5, now we will draw the required counter circuit.

# LOGIC DIAGRAM

![assignment output](https://github.com/pradeepsiva20/Simulation-project--Digital-Electronics/assets/120539823/7c441607-69ce-416e-8c22-b0c217082344)

# STATE TABLE 

![Screenshot 2023-06-10 182217](https://github.com/pradeepsiva20/Simulation-project--Digital-Electronics/assets/120539823/e1074b63-0f25-41c5-9830-71d8eba04118)


# NETLIST DIAGRAM

![netlist](https://github.com/pradeepsiva20/Simulation-project--Digital-Electronics/assets/120539823/5ebd0178-1ab2-4868-9306-c66692d154ef)


# TIMING DIAGRAM

![timing diagram for assignment](https://github.com/pradeepsiva20/Simulation-project--Digital-Electronics/assets/120539823/6385f812-3cbb-4d1c-bb00-7d8ebf4ce134)

# PROGRAM
```
module mod7(clk,reset,count);
input clk,reset;
output reg[2:0]count;
always@(posedge clk)
begin
if (reset)
    count <= 3'b000;
else
begin
    case(count)
	     3'b000 : count <= 3'b001;
	     3'b001 : count <= 3'b010;
	     3'b010 : count <= 3'b011;
	     3'b011 : count <= 3'b100;
	     3'b100 : count <= 3'b101;
	     3'b101 : count <= 3'b110;
	     3'b110 : count <= 3'b000;
   endcase
  end 
 end
endmodule
```

# REFERENCE
https://youtu.be/LF_Ll_EFl00
