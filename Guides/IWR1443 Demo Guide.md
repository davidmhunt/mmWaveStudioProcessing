# FLASHING THE BOARD

1. Ensure the board is disconnected from power.
2. Move the jumpers (black covers on the pins) to pins SOP0 and SOP2.
3. Connect the red board to power and USB.
4. Open UniFlash and load `C:\ti\mmwave_sdk_02_01_00_04\packages\ti\demo\xwr14xx\mmw` into Meta Image 1.
5. Go to "Settings & Utilities" and change the COM port to COM3 (or whichever is the XDS110 Class Application/ User UART port, you can check in device manager under Ports).
6. Go back to program and click "Load Image".

Done

^^refer to section 4.2 of the MMWAVE SDK USER GUIDE for more info.

# STARTING THE DEMO

1. Disconnect the board from power.
2. Remove the jumper from SOP2 (there should only be a single jumper on SOP0).
3. Reconnect the board to power.
4. Open [mmWave Demo Visualizer](https://dev.ti.com/gallery/view/mmwave/mmWave_Demo_Visualizer/ver/2.1.0/) on Google Chrome.
5. Click "Options" -> "Serial Port" at the top of the screen and change the CFG_port to COM3 (the XDS110 Class Application/ User UART port) and the DATA_port to COM4 (the XDS110 Class Data Port).
6. Click OK.
7. Click "SendConfig to mmwave device".

Finished!

^^refer to section 1.3 onwards of [MMWAVE SDK USER GUIDE](https://www.ti.com/lit/ug/swru529c/swru529c.pdf?ts=1716374263748), or the mmwave demo visualizer guide, for more info (we just did 1.2).
