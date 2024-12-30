## How to Flash Firmware
1. Connect the keyboard to the computer by USB
2. Double-click the `RESET` key to enter BootLoader mode. (At this point, you can see a new USB flash disk named nice！Nano)
3. We just need to put the new firmware into the first layer directory of this USB drive. 
**Note: Do not delete any files from the USB drive**

BootLoader can also be by triggering the `&BootLoader` keycode through a combination of keys. 
After modifying the keymap, you can get a new firmware.

> Flash all files that has "left" keyword in the left keyboard and "right" keyword on right keybaord

* Updating firmware for the keyboard also need connecting a USB cable.
* The setting_reset firmware’s function is to clear the connection configuration of the left and right keyboards.

## How to modify keymap
1. Open the project repository you forked. 
2. Find the eyelash_sofle.keymap file (The location is project name → config folder → eyelash_sofle.keymap)
3. Enter and modify it.
4. You can directly modify the key code in the file.

## How to generate the new firmware as you need
The keyboard has many functions that can be modified. I suggest understanding the functions of the keyboard before modifying the firmware. You should first take the time to understand the existing functions of the keyboard and familiarize yourself with the characteristics of keyboard operation. Afterwards, summarize your modification requirements for the original functions. There are many ways to create ZMK keyboard firmware, such as installing the ZMK compilation environment locally and using GitHub's codespace. I recommend the simplest method, which is to use the git action feature on GitHub to compile new firmware.

1. Fork this repository
2. Now click the `action` into a new page.
3. Click the `I understand workflows,go ahead and enable them`
4. Click on the option bar on the left. github/workflow/guil.yml
5. Click the `run workflow` button
6. Click the Run workflow
7. The page content will refresh to look like the image above, with yellow dots indicating that the firmware is being compiled. Please wait patiently for about 10 minutes.
8. Turning green to √ indicates that the compilation has been completed. Then click on this GitHub/workflows/build.yml
9. Click on the download icon in the bottom right corner of the above image to download the newly compiled firmware compressed file and decompress it. The files in the folder are the left and right hand firmware.
> or use a third-party graphical [tool](https://nickcoutsos.github.io/keymap-editor/) to modify the keymap.
10. Flash it in your keyboard.
