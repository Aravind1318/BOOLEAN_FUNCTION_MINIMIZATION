# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: ARAVIND P
RegisterNumber: 212224240015

*/
```

```py
module bool_func_min (
    input  wire A, B, C, D,
    input  wire W, X, Y, Z,
    output wire F1,
    output wire F2
);

    wire X1, X2, X3, X4, X5;
    wire X6, X7, X8, X9, X10;

    assign X1 = (~D) & (~C) & (~A) & (~B);
    assign X2 = (D) & (C) & (~A) & (~B);
    assign X3 = (D) & (~C) & (A) & (B);
    assign X4 = (~D) & (C) & (A) & (~B);
    assign X5 = (A) & (B) & (~C) & (~D);
    assign F1 = X1 | X2 | X3 | X4 | X5;

    assign X7 = Z | (~X) | (~Y);
    assign X8  = W & X & Y;
    assign X9  = (~Z) & X & (~Y);
    assign X10 = Z & X & Y;
    assign X6  = (~Z) & (~X) & Y;
    assign F2 = X6 | X7 | X8 | X9 | X10;

endmodule

```


**Output:**
![image](https://github.com/gauthamkrishna7/BOOLEAN_FUNCTION_MINIMIZATION/assets/141175025/86cc988b-b5fd-4693-a0a5-4a879656e903)

**RTL DIAGRAM**
<img width="743" height="889" alt="Screenshot 2025-09-11 143200" src="https://github.com/user-attachments/assets/0b6f384e-8a0a-49fe-817d-bc3d29848d9d" />

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

