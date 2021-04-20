# scd-bin-crc-cli (Qt C++)
Append CRC16 (16 bit CRC) to a bin file and set the file to the required size

Usage: bin-crc-cli <filename> <size>
  
## Params  

<b>filename</b>: source binary filename <br>
<b>size</b>: require size of destination file (crc included). <br><br>
If the destination size exceed the size of the original file, empty space at the end of file will be filled with FF, and the CRC will be added at the end of file.The size of the crc is 16 bits. The size of the space filled with FF is equal to <size> - 2 bytes. The destination size must be at least equal to original size + 2 bytes (CRC size), the remaining bytes (if any) will be fileld with FF.

This is useful to add a CRC16 to a firmware binary file.
