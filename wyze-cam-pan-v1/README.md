# Wyze Cam Pan V1 (WYZECP1)

# This image will upgrade your camera from factory firmware to Thingino. Don't try to use this for upgrading afterwards!

This was a popular model for a long tiem and while I don't recommend buying a new one today, lots of folks already have them and they are plentiful in the used market.
Installation video: https://youtu.be/Y4oC-Tg-Rdw

If you have trouble, jump on our Discord channel and we'll help you out!

# This process IS reversible

The first step of this installer will create a backup of your factory firmware, which can be used to revert back to Wyze if you need to.
The factory firmware file is named combined_backup.bin and will be in WYZE_BACKUP_xxxxx/
This backup is unique PER CAMERA, so if you don't save it somewhere yourself you won't be able to revert.

The images in the installers are updated once a week, you probably want to do a full upgrade after installing!

# Installation Steps

1. Download the zip file for the wyze-cam-pan-v1 from this repository
2. Use a sd image burning software such as Balena Etcher to write the image to your sd card (any card 128MB or larger)
3. Power off your camera and insert the sd card, thn power it on while holding down the SETUP button
4. Keep holding SETUP until the light turns blue, then release!
5. Wait around 3-4 minutes and you should see the camera's new wireless network for provisioning it.
6. After setting up the camera in webui, make sure to do a full update to current firmware as the included files are only updated periodically.

# Notes

If you are flashing multiple cameras, you need to copy and store the factory firmware backup file (combined_backup.bin), then use
your sd image burner to burn a fresh installer each time.

# Reversal Steps

To revert back to the stock Wyze firmware:

1. Ensure you're using the `combined_backup.bin` file that was generated from this exact camera. The files are not interchangable between came>
2. Copy `combined_backup.bin` from the `WYZE_BACKUP_xxxxx/` folder to the root of the SD card.
3. Rename `combined_backup.bin` to `autoupdate-full.bin`. This should be the only file on your SD card. You do not need any `.sha256` file.
4. Insert the SD card into your camera and plug in the power cable.
5. After a couple minutes the Wyze firmware will be restored. You do not need to manually reboot the camera.
6. When you press the `SETUP` button on the camera you'll get the original Wyze "Ready to connect" audio prompt.
