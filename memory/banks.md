# Banks

Although the Game Boy only has 64KB of addressable memory some cartridge's have 2 or more megabytes of memory. Because there is only a single address space the Game Boy makes use of **banks** to expand it's memory size.

### How do banks work?

Every cartridge can have a variable **ROM** size. A cartridge can also provide it's own onboard **RAM**. Refering back to the memory map, area *$0000* - *$3FFF* always refers to the first 16KB of the cartridge ROM, or *bank 0*, of the cartridge. The next 16KB (*$4000* - *$7FFF*) is for the switchable ROM bank. A cartridge can have as many 16KB banks as they want. To facilitate this switch every cartridge contains a **Memory Bank Controller** (MBC). The MBC handles swapping area *$4000* - *$7FFF* so that it refers to a seperate piece of the cartridge ROM.

Even though the MBC allows for switching it is far from convinient. It can quickly become a pain because all bank switching must be done explicitly. A 2MB cart would have over 100 usable memory banks to keep track of.

A cartridge can also come with up to 4 8KB banks of RAM for a total of 32KB additional memory.

### Controlling the MBC

To switch banks the MBC is mapped to specific memory. As there are quite a few MBC configurations refer to this [page](http://gbdev.gg8.se/wiki/articles/Memory_Bank_Controllers) if you are interested in the specifics.