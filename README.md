The NorthStar Horizon is a S-100 bus Z80 computer from 1977. This ROM monitor
was created as part of a restoration project. The initial need was a diagnostic
to isolate and troubleshoot basic hardware problems. The minimum hardware
required for this ROM was only the Z80 CPU and console serial port. Basic
function without memory was a design goal to assist with memory troubleshooting.
Memory from this era was a common source of failure for many retro computers.

Design requirements:
 
            1) No RAM memory, which includes no stack.
            2) Relative code, no fixed addressing.
            3) Modified Z80 CPU uses ROM 2716, 2048 bytes max size

Features:

            1) Map Memory 
            2) Test Memory
            3) Display Memory
            4) Edit Memory
            5) Go to address
            5) Boot - E800
            6) Fill Memory
            7) Loop address - for testing
            8) Intel-HEX load 

Assembler:

Develment environment was Ubuntu using z80asm. No preprocesser in this version which
should make it easier to port to other z80 assemblers.
For example:

           $ z80asm -onsz80rom.bin -lnsz80rom.lst nsz80rom.mac

