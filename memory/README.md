# Memory

The Game Boy uses a single address space for communicating with internal hardware, I/O and general storage for the programmer. With the 16-bit address bus on the CPU this allows for 64KB of address space shared between every device. 
  

Here's how this 64KB is divided up

### Memory Map

| Memory Location | Use |
| --------------- | --- |
| $FFFF       | Interrupt Enable Flag |
| $FF80-$FFFE | Zero Page - 127 bytes | 
| $FF00-$FF7F | Hardware I/O Registers |
| $FEA0-$FEFF | Unusable Memory |
| $FE00-$FE9F | OAM - Object Attribute Memory |
| $E000-$FDFF | Echo RAM - Reserved, Do Not Use |
| $D000-$DFFF | Internal RAM - Bank 1-7 |
| $C000-$CFFF | Internal RAM - Bank 0 |
| $A000-$BFFF | Cartridge RAM |
| $9C00-$9FFF | BG Map Data 2 |
| $9800-$9BFF | BG Map Data 1 |
| $8000-$97FF | Character RAM |
| $4000-$7FFF | Cartridge ROM - Switchable Banks 1-xx |
| $0150-$3FFF | Cartridge ROM - Bank 0 |
| $0100-$014F | Cartridge Header Area |
| $0000-$00FF | Restart and Interrupt Vectors |

Before we go into the specifics of each section you might have noticed multiple memory areas refering to *Banks*. Let's see what these are first.

<hr>
(Memory Map)[http://gameboy.mongenel.com/dmg/asmmemmap.html] from [Duo's Gameboy Dev](http://gameboy.mongenel.com/)