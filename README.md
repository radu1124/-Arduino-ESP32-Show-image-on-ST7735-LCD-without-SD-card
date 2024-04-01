In this project I am using an ESP32 board and a ST7735s LDC display. 
The goal of this project is to render an image on the display without using an SD card. 
Firstly, we will put the ESP32 and the display on the breadboard.
Connect the ESP32 to the breadboard's ground.
Then, we will connect the display pins, as showed in the photo below:



![image](https://github.com/radu1124/-Arduino-ESP32-Show-image-on-display-without-SD-card/assets/85763672/3b7d7d28-c904-4ff4-8693-026c991e180c)


ESP32 pins:

![image](https://github.com/radu1124/-Arduino-ESP32-Show-image-on-display-without-SD-card/assets/85763672/61f99c5d-c330-4328-837c-7ccdd82a667e)


When we connect the ESP32 to USB, the screen should turn on, but show nothing.
Next, we will need a softare to convert the image we want to show on the display to individual pixel color codes.
I personally chose lcd image concverter. You can download it from here:
https://sourceforge.net/projects/lcd-image-converter/

We will need to know the display's resolution and it's capabilities.
My display can show 16bit images, and has a max resolution of 128x128, so i will encode the image according to this specifications.

The image that will appear on the screen:

![mini_nasa](https://github.com/radu1124/-Arduino-ESP32-Show-image-on-display-without-SD-card/assets/85763672/e784f033-a621-47ec-958a-d3092f191ff0)


Paste the code of the image between the brackets:

const uint16_t imageData[IMAGE_WIDTH * IMAGE_HEIGHT]{
//insert image code here
}

Upload the code on the board and keep the boot button pressed until the code starts uploading.
Then press the reset button on the board, and the image should appear on the display.
If the image is messed up, change the encoding setting on the lcd image converter software.

Final result:


![WhatsApp Image 2024-03-29 at 16 29 38](https://github.com/radu1124/-Arduino-ESP32-Show-image-on-display-without-SD-card/assets/85763672/908f73c9-1543-40cf-a1ec-04966c495aaa)

