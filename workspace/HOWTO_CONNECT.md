# Prerequisites:

1. Make sure that ADB tools are installed on your pc
2. Device must have Developer Options activated, Debug USB enabled and Install Via USB enabled
3. Device and PC MUST be connected to the same network
4. Take a note of the Device WiFi IP going to WIFI -> Advanced

# Connection -- On the host

1. Connect device to PC via USB
2. Run `adb devices`
3. Authorize the popup that will be shown on the device
4. Run `adb tcpip 5555 && adb connect <Device WiFi ip>:5555 && adb devices`

# Connection - On Docker

1. Run `adb devices`
2. Run `adb connect <Device WiFi IP>:5555 && adb devices`
3. Authorize device with the popup that will be shown on the device

If device is unauthorized run 
`adb kill-server`
`adb connect 192.168.0.5:5555`
`adb devices`

4. Unplug the usb and run flutter doctor to see if everything is fine