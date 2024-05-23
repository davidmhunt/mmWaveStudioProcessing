# FORMAT FIRMWARE

This step should be done each time you need to put new firmware on the radar, e.g., before you run the data capture board.

1. Ensure the power is disconnected from the radar board and move the jumpers (black sleeves) to pins SOP0 and SOP2, leaving SOP1 exposed.
2. Connect power and USB, open UniFlash and connect to the board (either click "detect" or AWR1443BOOST).
3. Go to "Settings and Utilities" and modify the COM port to the one your radar board is using (can be found by opening Device Manager, clicking under Ports, use the one that says XDS110 Class Application/User UART).
4. Click "Format SFLASH".

Done!

# DATA CAPTURE

## HARDWARE CONFIG

1. Ensure the switch on the data capture board is set to "Radar_5V_in".
2. Connect the power supply and USB port on the IWR1443 to the PC, and connect the Ethernet and the Radar_FTDI (right USB port) to the PC.
3. Make sure the two boards are connected (should already be).

## MMWAVE STUDIO USAGE

1. Ensure power is disconnected from the radar board and move the jumpers to pins SOP0 and SOP1.
2. Reconnect power and open mmWave Studio.
3. Under "RS232 Operations" ensure the COM Port is set correctly (same as in format firmware).
4. Load the proper firmware files into BSS FW and MSS FW:
   - (a) BSS FW should be at `C:\ti\mmwave_studio_02_01_01_00\rf_eval_firmware\radarss\xwr12xx_xwr14xx_radarss.bin`
   - (b) MSS FW should be at `C:\ti\mmwave_studio_02_01_01_00\rf_eval_firmware\masterss\xwr12xx_xwr14xx_masterss.bin`
5. 
   - (a) Under "Reset", click "Set".
   - (b) Under "RS232 Operations", click "Connect".
   - (c) Click "load" for BSS FW, then MSS FW.
   - (d) Click "SPI Connect".
   - (e) Click "RF Power-Up".
6. Go through "StaticConfig", "DataConfig", "TestSource", and click "Set" wherever possible.
7. Go to "SensorConfig", and click set in the following order: "Sensor Configuration", "Chirp", "Frame".
8. Click "Set Up DCA1000" on the left side of your screen, then click "Connect, Reset, and Configure" on the popup.
9. Go under "Capture and Post Processing", and click "DCA1000 ARM".

You're done setting up! Clicking "Trigger Frame" will get you a data snapshot, which you can view once it's finished by clicking "PostProc". If "PostProc" throws an error, you might've forgotten to click "Set" on something.
