# STM32F1 SPI HAL DMA ST7735 Display drivers, improved DMA calls

The checks for busy SPI TX have now been placed just before each TX to the ST7735.
In this way all the graphic functions can give back control to the mcu immediately while the DMA transfer is still executing, resulting in more time for the mcu to do other non-graphic stuff.

I modified the DemoTFT code to run as a benchmark without pauses. The demo running time in portrait mode went from 1850ms to 1713ms.
I expect an even bigger speed increase in a multitasking environment (FreeRTOS)


[![](https://img.youtube.com/vi/jwexGqwaj6g/0.jpg)](https://youtu.be/jwexGqwaj6g "DEMO")

 Forked from https://github.com/ScarsFun/STM32F103C8T6_cubeIDE_ST7735_1.8_DMA
 Fork from : https://stm32withoutfear.blogspot.com/2019/03/stm32-lcd-st7735.html


