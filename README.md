 ## EXP 2:
# BOOLEAN_FUNCTION_MINIMIZATION

 ## NAME : ABISHEIK
 ## REG NO: 212223040005
 
**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

```
module experiment2(a, b, c, d, w, x, y, z, f1, f2);
input a, b, c, d, w, x, y, z;
output f1, f2;
wire x1, x2, x3, x4, x5, y1, y2, y3, y4, y5;
assign x1 = ((~a) & (~b) & (~c) & (~d));
assign x2 = (a & (~c) & (~d));
assign x3 = ((~b) & (c) & (~d));
assign x4 = ((~a) & b & c & d);
assign x5 = (b & (~c) & d);
assign f1 = x1 | x2 | x3 | x4 | x5;


assign y1 = (x & (~y) & z);
assign y2 = ((~x) & y & z);
assign y3 = ((~w) & x & y);
assign y4 = (w & (~x) & y);
assign y5 = (w & x & y);
assign f2 = y1 | y2 | y3 | y4 | y5;
endmodule
```


**RTL realization**

**Output:**

**RTL**

![Screenshot 2025-04-24 112019](https://github.com/user-attachments/assets/528bf65d-2a8e-4928-b518-dbe0d5d54365)
![Screenshot 2025-04-24 112028](https://github.com/user-attachments/assets/58846d25-9200-40f7-83a2-41f8e4dfa5be)


**Timing Diagram**


![image](https://github.com/user-attachments/assets/eb11d821-c973-40e6-921f-e5661c40354e)


**Result:**
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

