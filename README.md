# Revilogat
A Verilog like HDL language used like assembly for selial logic cells (SLC) FPGAs. Serial logic cells are cells that use memory to serialy process logic. It can be converted to Verilog. By default compiler compile to simple NOR SLC assembly.
The assebbly file has 3 secrions:
1. Data
2. Cache
3. Code
(Strictly in this order).
The code section is separated from the others
The compilation can be also without cache section (with flag -b or --bare).
