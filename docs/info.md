3-Bit Adder-Subtractor

---

## How it works

This project implements a *3-bit Adder-Subtractor* circuit using *Full Adders* and *XOR gates*.

* The circuit can perform both *addition* and *subtraction* depending on the control input CTRL.
* Each Full Adder receives three inputs: A[i], B[i] XOR CTRL, and the carry-in (Cin).
* The CTRL signal selects the operation:

  * CTRL = 0: The XOR gates pass B[i] unchanged, so the Full Adders perform *A + B*.
  * CTRL = 1: The XOR gates invert B[i] and the initial Cin is set to 1, effectively adding A + (~B + 1) which equals *A - B* (2’s complement subtraction).
* The outputs are S2, S1, S0 (the 3-bit sum or difference) and Cout (the carry or borrow).

---

## How to test

1. Provide 3-bit binary inputs A2 A1 A0 and B2 B1 B0.
2. Set the control input CTRL:

   * CTRL = 0: The circuit outputs the *sum (A + B)*.
   * CTRL = 1: The circuit outputs the *difference (A - B)*.
3. Observe the output values:

   * S2 S1 S0 → 3-bit result (sum or difference).
   * Cout → Carry (for addition) or Borrow (for subtraction).

You can verify correctness by comparing the circuit outputs with manual binary addition and subtraction calculations.

---

## External hardware

* No external hardware is required if tested in simulation (Verilog/VHDL/Logisim).
* If implemented on FPGA or breadboard:

  * *7-segment display or LEDs* can be used to visualize outputs.
  * *Switches or buttons* can provide input values for A, B, and CTRL.

---

Do you also want me to *make a Verilog code* for this 3-bit Adder-Subtractor with testbench in the same format?
