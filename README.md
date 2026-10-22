![Neural data logger](photo.jpg)
MSPM0G3507 and Intan RHD2132 
4 neural channels at 20 kHz (50 µs period) and 3 auxiliary channels at 100 Hz, inserted every 200 neural samples 
●
Intan SPI0 acquisition using DMA-driven transfers and CPU-managed ping-pong buffering 
Each buffer is 16 SD sectors, 8,192 bytes 
Bypasses filesystem overhead using continuous CMD25 raw-sector writes, with a recording-length header and reserved diagnostic sectors enabling structured MATLAB reconstruction and validation.
●
SPI1 TX DMA moves each 512-byte sector from RAM while RX DMA discards the return bytes 
CPU handles the start token, CRC, card-busy, and sector count 
●
Measured 16-sector write latencies as low as approximately 7 ms, with a maximum observed 50.75 ms during extended testing 
Zero overruns under variable card latency 
MicroSD SPI1 interface configured for 8 MHz operation 
●
Recording power: 58 mA and 192 mW at 3.3 V over one minute 
●
Head-mounted PCB with Omnetics A22016-001 connector and MSPM0G1507 (ported MSPM0G3507 dev board to MSPM0G1507) 
Awaiting fabrication 
