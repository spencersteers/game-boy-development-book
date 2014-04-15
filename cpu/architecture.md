# Architecture

The Sharp LR35902 is often described as a hybrid between the [Intel 8080](http://en.wikipedia.org/wiki/Intel_8080) and [Zilog Z80](http://en.wikipedia.org/wiki/Zilog_Z80).

Originally the Z80 was designed to be binary compatible with the 8080. A program using the 8080 instruction set can run on a Z80 without modification.

### Features
- 16-bit address bus (64K addressable memory)
- 8-bit data bus
- 8-bit accumulator
- 6 8-bit general purpose registers
    + Can combine registers to make a 16-bit general purpose register: `B` & `C` = `BC`
- 16-bit stack pointer
- 16-bit program counter
- 8-bit status flag register

<hr>
[![Z80 Architecture Diagram](https://raw.github.com/spencersteers/game-boy-development-book/master/assets/z80-arch.png)](https://raw.github.com/spencersteers/game-boy-development-book/master/assets/z80-arch.png)
*There are a couple things on the Z80 diagram that the LR35902 does not have. Their differences will be discussed in the next section.*
