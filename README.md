# Aim:
To simulate and synthesis full subtractor using Vivado 2023.2.

# Software Required:
Vivado 2023.2.
# Procedure:
1. Open Vivado: Launch Xilinx Vivado software on your computer.

2. Create a New Project: Click on "Create Project" from the welcome page or navigate through "File" > "Project" > "New".

3. Project Settings: Follow the prompts to set up your project. Specify the project name, location, and select RTL project type.

4. Add Design Files: Add your Verilog design files to the project. You can do this by right-clicking on "Design Sources" in the Sources window, then selecting "Add Sources". Choose your Verilog files from the file browser.

5. Specify Simulation Settings: Go to "Simulation" > "Simulation Settings". Choose your simulation language (Verilog in this case) and simulation tool (Vivado Simulator).

6. Run Simulation: Go to "Flow" > "Run Simulation" > "Run Behavioral Simulation". This will launch the Vivado Simulator and compile your design for simulation.

7. Set Simulation Time: In the Vivado Simulator window, set the simulation time if it's not set automatically. This determines how long the simulation will run.

8. Run Simulation: Start the simulation by clicking on the "Run" button in the simulation window.

9. View Results: After the simulation completes, you can view waveforms, debug signals, and analyze the behavior of your design.
# Truth Table and Circuit Diagram
![image](https://github.com/RESMIRNAIR/FULL_SUBTRACTOR/assets/154305926/351addef-f7bb-4862-9817-616a41b4c882)
![image](https://github.com/RESMIRNAIR/FULL_SUBTRACTOR/assets/154305926/906152b8-63bc-4f70-9132-6b6b4420b22d)
![image](https://github.com/RESMIRNAIR/FULL_SUBTRACTOR/assets/154305926/7d480140-153a-4a7e-a6d2-5323c6bd4974)
# Program
```
module full_subtractor(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
wire w1,w2,w3,w4;
xor s1(w1,a,b);
not s3(w2,w1);
not s4(w4,c);
and s5(y,w4,b);
xor s2(diff,a,w1);
and s6(w3,w2,a);
or (borr,y,w3);
endmodule
```
# Output
![full subtracter](https://github.com/j-gugan/FULL_SUBTRACTOR/assets/163828735/5f2ffdb4-da5b-432b-aa11-932caacdb9f6)
# Result:
Thus, Full Subtracter using Vivado 2023.2 is simulated and synthesised.
