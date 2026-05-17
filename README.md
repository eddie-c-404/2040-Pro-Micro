# 2040-Pro-Micro
An open source Arduino Pro Micro but with an RP2040.

<img width="3642" height="1937" alt="rp2040 pro micro2" src="https://github.com/user-attachments/assets/1b6afabe-f6fc-4a29-9a56-2a2666dbaed0" />

**Overview:**

The Arduino Pro Micro is a small-form-factor, useful, and pretty cool microcontroller that's missing just one thing: some more juice!!! Unfortunately, it only runs at 16 MHz and is an 8-bit CPU. Introducing the RP2040 Pro Micro, it's just like the Arduino in every single way, but it includes some more powerful components and better specs. This project originates from a problem I had a while ago. 11-year-old me had just made his finest electronics project, A flight control stick to play flight sims on his MacBook (IDK why, but I really enjoyed those back then). He had started with an Arduino Nano, and after a couple of hours of wiring and searching for how to code, he arrived at his final step: testing it. As you might be able to tell, it didn't work at all. Matter of fact, he spent more time trying to get it to work than he spent building it. He googled and googled and learned about HID, and how the ATmega 328P doesn't have that. So, unfortunately, all other solutions were out of his budget, so he moved on to blinking LEDs. Now, 3 years later, I created this to be a substitute for the heavily underpowered Arduino Pro Micro and to achieve my goal of creating a flight stick (ig).    

<img width="3642" height="1937" alt="rp2040 pro micro3" src="https://github.com/user-attachments/assets/74c10366-9dfd-4371-8eae-4b9c740b0ce7" />

**Specs:**

*CPU:* RP2040 featuring dual ARM Cortex-M0+ (32-bit ARMv6-M) cores running at 133 MHz, 264 KB of internal SRAM.

*Flash:* 64 Mbit (8 MB) of external flash NOR Memory IC

*Connectivity:* USB-C port supporting up to USB 2.0 speeds for data transfer.

*I/O:* 24 pins with 20 I/O pins and 4 power pins. (Note that pins do **NOT** have +5v tolerence).

*Buttons:*  BOOT SELECT button, RESET button.

*Power:* USB-C for +5v input, MCP1700xx LDO for voltage regulation (+3.3v), max 250 mA output overall.
 
<img width="3642" height="1937" alt="rp2040 pro micro" src="https://github.com/user-attachments/assets/0da53aa4-aaa4-4bed-b9a5-9de3c573aaf8" />

**BOM and other pictures:**


<img width="582" height="1240" alt="image" src="https://github.com/user-attachments/assets/1f2070d4-646d-4a0d-a566-35400eaa39e3" />

<img width="2563" height="1812" alt="image" src="https://github.com/user-attachments/assets/a8a47aa3-7c12-40e2-8159-f3d1bf2d42c8" />



| Name         | Reference on pcb | LCSC Part # | Footprint     | Price |
|--------------|------------------|-------------|---------------|-------|
| 1uF          | C1/C12           | C15849      | C0603         | 0.39  |
| 0.1uF        | C2-C11/C18/C17   | C60474      | C0402         | 0.1   |
| 10uF         | C13/C14          | C19702      | C0603         | 0.4   |
| 33pF         | C15/C16          | C70465      | C0402         | 0.36  |
| USB-C        | J1               | C165948     | SMD           | 0.85  |
| GPIO pins    | J2/J3            | C6332195    | 1x12          | 0.4   |
| SWD pins     | J4               | C32713269   | 1x03          | 0.11  |
| Crystal      | Y1               | C9002       | SMD3225-4P    | 0.73  |
| Buttons      | SW1/SW2          | C720477     | SMD,4x3mm     | 0.55  |
| 10k          | R6/R8            | C98220      | R0603         | 0.15  |
| 5.1k         | R1/R2            | C2907044    | R0603         | 0.12  |
| 27ohm        | R3/R4            | C2907021    | R0603         | 0.1   |
| 1k           | R5/R7            | C22548      | R0603         | 0.15  |
| RP2040       | U1               | C2040       | LQFN-56(7x7)  | 0.95  |
| MCP1700xx    | U2               | C39051      | SOT-23        | 1.88  |
| W25Q64JVSSIQ | U3               | C97521      | SOIC-8-208mil | 1.65  |
| Total        | X                | X           | X             | 8.89  |

**General Insruction:**

If you would like to get this PCB manufactured, you can download the rp2040_pro_micro.zip file. When your pcb manufacturer asks for a gerber file, upload that.
If you would like to copy the schematic, you can but take note that the pins labled left pins are the rigth pins and vice versa.
The BOM file is the BOM.csv, the CPL file is positions.csv.
If you want to use the already existing kicad files, you can use the .kicad_pro (entire proj.), the .kicad_sch (schematic), or the .kicad_pcb (the pcb).


