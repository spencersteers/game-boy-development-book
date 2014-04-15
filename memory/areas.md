# Areas

Let's look at a few areas of the memory map

## Hardware I/O Registers: $FF00-$FF7F 

### Joypad

All joypad input is handled at `$FF00`. Of the 8 bits only 0 - 5 are used. Each bit is mapped to **Ports** 15 - 10. When P15 is low then P13 - P10 return d-pad data. When P14 is low then P13 - P10 return button data.

Below is the matrix illustrating this

|        | P15 | P14 |
| ------ | ------ | ------ |
| P13 | Right | A |
| P12 | Left | B |
| P11 | Up | Select |
| P10 | Down | Start |

If you set P15 low `%00010000` then the value `%00001000` cooresponds to **right** being down. 

Here is a quick example in assembly:

```nasm
    LD A,$20       ; P15 ($20) (%00100000)
    LD ($FF00),A   ; select P14 by setting P15 high
    LD A,($FF00)
    LD A,($FF00)   ; wait a few cycles to recieve input
    LD A,($FF00)   ; Accumulator holding button presses
```
