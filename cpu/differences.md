# Differences Between LR35902 and 8080/Z80

Although similar to the Z80 the LR35902 has a few differences that are worth noting:

### The LR35902 has...
- `0xCB` extension opcode
    + The `0xCB` instruction signals that the next byte is an additional operation
    + The 8080 did not use `0xCB` for an opcode so the Z80 was free to use it to facilitate additional instructions
- Bit-Manipulation opcodes (only Z80 extended instruction that made it)

### The LR35902 is missing...
- Seperate address space for input and output
- Registers `IY` and `IX`
    + Used for common base + offset memory addressing
-  Alternate (Shadow) Registers for every register
    +  `A'`, `B'`, `C'` ...
    +  Used to speed up system start time
-  Extended Z80 instructions (except for bit-manipulation)

