🚀 Simulating a Verilog-A Diode Model in Cadence ADE

This guide walks you through the steps to simulate a Verilog-A diode model in Cadence Virtuoso using ADE (Analog Design Environment).
📝 Diode Model Overview

The diode model is implemented using Verilog-A, which is a hardware description language used for analog and mixed-signal circuit simulation. The model represents the diode's current-voltage relationship based on the Shockley diode equation.


The Verilog-A code defines the following parameters:

    Is: Saturation current (A)

    N: Ideality factor (dimensionless)

    Vt: Thermal voltage (V)

The current through the diode is modeled as:

I = Is * (exp(V / (N * Vt)) - 1)

Where V is the voltage across the diode, Is is the saturation current, N is the ideality factor, and Vt is the thermal voltage.
📁 Files Included
File Name	Description
diode.va	Verilog-A code for the diode model
🚀 Steps to Simulate the Diode Model in Cadence ADE
1. Create a New Cellview in Cadence Virtuoso

    Open Cadence Virtuoso and launch the Library Manager.

    Choose or create a new library for the diode model.

    Create a new Cellview:

        File → New → Cellview

        View Name: veriloga

        Tool: Select Verilog-A

    Paste the Verilog-A code into the editor and save it. You can use the code provided in this repository.

2. Instantiate the Diode Model in a Schematic

    Open your testbench schematic (or create a new one).

    In the schematic editor, use the Component tool to place the diode symbol (which will be generated after you compile the Verilog-A code).

    Wire the diode to the other components in your circuit (e.g., voltage sources, resistors).

![diode](https://github.com/user-attachments/assets/86e9e551-74f9-4994-aeed-f841c0c34b73)

3. Set Up Simulation Environment

    Open ADE: In the Cadence Virtuoso environment, open Analog Design Environment (ADE).

    Select Simulation Type: Choose the simulation type (e.g., DC, Transient, etc.).

    Configure Inputs and Outputs:

        In the Simulation Setup window, configure the simulation options like the input stimulus (voltage source) and the desired output (e.g., current through the diode or voltage across it).

    Select Outputs to Plot: Choose the parameters you want to observe, such as the voltage and current of the diode.

4. Run the Simulation

    In the ADE window, click Simulation → Run to start the simulation.

    Monitor the results in the Waveform Viewer.

5. Analyze Results

    You can plot the current-voltage (I-V) characteristics of the diode by observing the voltage across and current through the diode.

    Use the Waveform Viewer to analyze the simulated data and compare the diode’s behavior to expected theoretical results.

![diode](https://github.com/user-attachments/assets/b55ef6c5-4b5a-455a-a2a6-8fa7d6ec159c)



💡 Notes

    Make sure that the parameters in the Verilog-A code (such as Is, N, and Vt) are adjusted according to the type of diode you are modeling.

    The thermal voltage (Vt) is typically around 25.9mV at room temperature for silicon diodes.

⚙️ Modify the Model

Feel free to modify this Verilog-A code to suit your needs. You can change parameters such as:

    Saturation Current (Is)

    Ideality Factor (N)

    Thermal Voltage (Vt)

---
