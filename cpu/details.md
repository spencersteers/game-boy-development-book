# Details

Here are some specifics on identifying and using the LR35902

### Registers

| Type | Name(s) |
| ---- | ------- |
| Accumulator (8-bit) | `A` |
| Status Flags (8-bit) | `F` |
| Program Counter (16-bit) | `PC` |
| Stack Pointer (16-bit) | `SP` |
| General Purpose (8-bit) | `B` `C` `D` `E` `H` `L`  |
| General Purpose (16-bit) | `AF` `BC` `DE` `HL` |

**Although you can use `AF` it is most commonly not used for general purpose but to push the accumulator/status state onto the stack**

### Status Flags
Each bit of the register `F` represents a specific state or **flag**

| Bit 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| ----- | - | - | - | - | - | - | - |
| unused | unused | unused | unused | Carry | Half-Carry | Subtract | Zero |

- Carry: Set when carry from bit 7 is produced from an arithmetic operation
- Half-Carry: Set when carry from bit 3 is produced from an arithmetic operation
- Subtract: Set when the instruction is subtraction
- Zero: Set when instruction result is 0
