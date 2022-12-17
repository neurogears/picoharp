# picoharp
A generic device that implements the harp protocol in a raspberry pico device

# Getting started

1. Upload the custom firmware to the pico:
   1. Unplug your pico from the USB.
   2. Click the `BOOTSEL` button.
   3. While clicking the `BOOTSEL` button, reconnect your pico.
   4. The device will be recognized as a general storage device. Simply drag and drop the firmware file [`./microharp/bin/firmware.uf2`](https://github.com/neurogears/microharp/blob/ee623f5dd82bded2a337b03fe4907185c3396ce9/bin/firmware.uf2) to the root folder.
   5. The pico will reset and the new firmware is now uploaded. This step should only be necessary once.
2. Upload the device code to the device:
   1. Install [Thonny](https://thonny.org/)
   2. Clone this repo.
   3. Connect your pico device to Thonny by selecting the appropriate COM port. pico will show up as two identical devices, you should use the lowest number COM port to upload your code.
   4. Replicate the structure of the repo in Thonny and upload the files to the pico. E.g.:

   ![FolderStructure](/assets/filestructure.png)

   5. Power cycle the device.

3. Interface with your pico from Bonsai.
   1. Open Bonsai and add a `Device(Harp)` operator;
   2. Select the COM port. It should be the highest COM port of the two made available by connecting the pico.
   3. You can now send/receive `HarpMessages` to/from the `Device` operator.

