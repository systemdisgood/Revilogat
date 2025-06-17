# Revilogat
A Verilog like HDL language used like assembly for selial logic cells (SLC) FPGAs. Serial logic cells are cells that use memory to serialy process logic. It can be converted to Verilog. By default compiler compile to simple NOR SLC assembly.

The assebbly file has 3 secrions:
1. Data
2. Cache
3. Code

(Strictly in this order).

The execution process is a serial process that ahain and again walking through the 3 sections by two heads: the code head and the data head. If the section is a code section, code head reads either instruction or address. If it is the instruction, the data head do NOR operation with 2 bits, rewriting accumulator bit and makind 2 bits step. If it is the address, the data head stores the accumulator bit by this address. It is useful to store this bits in the cache section serialy and then when the data head reaches the cache srction, store bits to the data secrion. The compilation can be also without cache section (with flag -b or --bare).
