# CNN Accelerator RTL (SystemVerilog)

A SystemVerilog hardware accelerator for one convolutional neural network (CNN) layer. It reads a 1024 × 1024 image from DRAM, runs 4 × 4 convolution, Leaky ReLU activation and 2 × 2 average pooling, and writes the result back to DRAM. Built for ECE 564 at NC State University (Fall 2025).

## Highlights

- **Pipelined datapath** with parallel multiply-accumulate units.
- **On-chip buffering** that keeps DRAM traffic low.
- **Burst-based DRAM interface** with a start/ready handshake.
- **Fast:** a full image takes about 1.05 million clock cycles.

## Verification

Simulated against the course testbench, which runs multiple datasets and compares the accelerator's output with golden reference results. The final design passes.

## Tools

SystemVerilog and QuestaSim.

## Author

Sanchit Varshney
