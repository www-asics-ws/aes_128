# aes_128
 AES (Rijndael) IP Core (128 bit version)

Description

Simple AES (Rijndael) IP Core. I have tried to balance this implementation and to trade
off size and performance. The goal was to be able to fit in to a low cost Xilinx Spartan
series FPGA and still be as fast as possible. As one can see from the implementation
results below, this goal has been achieved ! Other Implementations of this standard with
different key sizes (192 & 256 bit) and performance attributes (like a fully pipelined
ultra-high-speed version) are commercially available from ASICS.ws. Even though no official
testing has been performed we believe that this core is fully complies to FIPS-197 (pdf).
For more information see the core documentation.

https://csrc.nist.gov/csrc/media/publications/fips/197/final/documents/fips-197.pdf


Features

    16 byte block size
    16 byte key size
    separate cipher (encrypt) block
    separate inverted cipher (decrypt) block
    incorporated key expansion module
    written in verilog


Sample Synthesis Results for the Cipher Block

    Technology	Size/Area	Speed/Performance
    Xilinx Spartan IIe XS2V200-6	3497 LUTs (74 %), 1026 Regs. (21 %)	101 Mhz (1.08 Gbits/sec)
    UMC 0.18u Std. Cell	38K Gates	265 Mhz (2.82 Gbits/sec)


Sample Synthesis Results for the Inverse Cipher Block

    Technology	Size/Area	Speed/Performance
    Xilinx Spartan IIe XS2V200-6	3393 LUTs (72 %), 883 Regs. (18 %)	85 Mhz (906 Mbits/sec)
    UMC 0.18u Std. Cell	50K Gates	235 Mhz (2.5 Gbits/sec)
