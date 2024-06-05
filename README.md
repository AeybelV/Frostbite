# Frostbite Development Board

Frostbite is a development board for hobbyists containing a RISC-V ESP32 Processor (ESP32 S3) and a Lattice Semiconductor iCE40UP5K FPGA.

The project is currently in progress and in its early stages. This project is first FPGA PCB; my motivation for the project is to gain knowledge about FPGA hardware design, as well as use the board to design another project: a custom logic analyzer.

## Roadmap

The follow is the stages of development that will be tested before arriving at a full solution

### Stage 1 - iCE40 Development Board (IN PROGRESS)

The first revision of the Frostbite board is a bare minimum board to get the FPGA portion of the board up and running. The board can allow for the FPGA to be programmed. The FPGA has a bootsel pin that indicates how it can be flashed: SPI directly or via SPI flash. The SPI Flash has breakout to allow external programmer to flash it, or use a FTDI chip to program from a PC host via serial.

### Stage 2 - ESP32

Once the FPGA board can be programmed and works functionally, the board will be expanded to setup a  ESP32 C-3 MCU. 

### Stage 3 - Integration

When FPGA and ESP functionality is both verified, modifications will be made to allow for both to work together. An external RAM chip will be shared between both to allow for shared memory access. In addition, the FPGA will continue to have direct SPI or SPI flash uploading; however the direct SPI can be from the MCU or from USB FTDI from a PC Host. In addition Pmod lines between the MCU and FPGA allow for I/O interfaces between the two.


