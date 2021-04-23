# Neural Network generator using TL-Verilog

This repo contains a blueprint implementation(WIP) of neural network architecture using an evolving Transaction-Level design methodology i.e., [TL-Verilog](https://www.makerchip.com/). 

  - <a href="http://www.makerchip.com/sandbox?code_url=https:%2F%2Fraw.githubusercontent.com%2Fvineetjain07%2FDNN_TL-V%2Fmaster%2Fnn.tlv" target="_blank" atom_fix="_">open in makerchip </a>
## Motivation

## Methodology

### Current Status

1. " [***nn.tlv***](nn.tlv) "
    - Complete *neuron* macro implementation with variable pipeline depths (from 0 to 5).
    - Complete *layer* macro implementation, which instantiates the specified number of neurons.
    - Complete memory(ROM) for weights and bias (without different values)

2. " [***gen_wb.py***](gen_wb.py) "
    - Python script for generating weigths and bias using Tensor-flow.
## TODO

1. Currently, weights and bias values are hardcoded and are identical for all neurons in memory. Hence, we need to import necessary parameters according to network configuration from the external mem file for each neuron.

2. The logic/code for I/O interafce and connection of layers is not parameterized using M4 (like a neuron, layer), and at present, it's fixed.

3. Add write ports in memory so that software can also change or manipulate the weights and biases value.

4. Add support for different Activation Functions (like, sigmoid, tanh, linear, softsign, etc.)

5. Currently, MAC (multiply and accumulate) operation uses Fixed-Point representation. We can add logic to support Floating-point, Posits, etc.

6. Add test cases for Verification of design.

## Contributions
This repo is WIP(work in progress) and may be moved to a different place in later stages. It contains a draft architecture and approach for neural-network generators using TL-Verilog.

The python script and  is taken from the following refernces.


Any kind of feedback or suggestions is highly appreciated.