
# Half Subtractor using Verilog

## Overview

A Half Subtractor is a combinational logic circuit that subtracts two single-bit binary numbers. It has two inputs:

- A (Minuend)
- B (Subtrahend)

It produces two outputs:

- Difference (D)
- Borrow (Bo)

## Truth Table

| A | B | Difference | Borrow |
|---|---|------------|--------|
| 0 | 0 |     0      |   0    |
| 0 | 1 |     1      |   1    |
| 1 | 0 |     1      |   0    |
| 1 | 1 |     0      |   0    |

## Boolean Expressions

Difference = A XOR B

Borrow = A' AND B

## Files

- `half_subtractor.v` - Verilog design
- `half_subtractor_tb.v` - Testbench
- `simulation_output.png` - Simulation result
- `waveform.vcd` - Waveform file

## Simulation

Compile

```bash
iverilog -o hs half_subtractor.v half_subtractor_tb.v
```

Run

```bash
vvp hs
```

Generate waveform

```bash
gtkwave waveform.vcd
```

## Expected Output

```
A B | Difference Borrow
0 0 |     0        0
0 1 |     1        1
1 0 |     1        0
1 1 |     0        0
```

## Author

Your Name