# Syndrome_Calculator

I’ve been working on a Syndrome Calculator (used in error-detection/error-correction like Hamming codes), and I decided to build the whole thing completely from discrete transistors — no ICs, no logic chips, just raw Boolean logic on breadboards.

The circuit computes the syndrome bits based on the input data(4bits) + parity bits(3bits) and can be used to detect single-bit errors. Every gate you see here (XOR, NAND, XNOR, NOT) is built from individual BJTs and resistors.

It’s messy, it’s huge, but it actually works!
Right now it outputs all the syndrome bits through the LED bar on the top board and green LED is for power status.

If anyone else here is into discrete logic, breadboard CPUs, or homebrew ECC circuits, I’d love to hear your thoughts or suggestions.

The attached Logic Schematics consists of 9 XOR gates which points out the wrong bit in binary, after that a 7 NAND gates decoder points out to the exact bit which later makes the XNOR gate act like inverter for the wrong bit and buffer for right bit.

Overall it takes 7bits as input in which 4 are data bits and 3 are parity bits.
