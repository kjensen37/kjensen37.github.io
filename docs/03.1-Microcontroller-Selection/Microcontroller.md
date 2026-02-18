## Microcontroller Selection

| ESP Info                                      | Answer | Help                                                                                                      |
| --------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------- |
| Model         | ESP32-S3-WROOM-1-N4    | Include the entire part number (leave off any letters at the end that specify the package type)   |
| Product Page URL     | [product page](https://www.espressif.com/en/products/socs/esp32-s3)      | Found on Espressif.com |
| ESP32-S3-WROOM-1-N4 Datasheet URL             | [datasheet](https://documentation.espressif.com/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf)     | Do not paste links directly into the table.  Use a [link](#)                                              |
| ESP32 S3 Datasheet URL                        | [datasheet](https://documentation.espressif.com/esp32-s3_datasheet_en.pdf)     | Has more detail on functions                                                                              |
| ESP32 S3 Technical Reference Manual URL       | [manual](https://documentation.espressif.com/esp32-s3_technical_reference_manual_en.pdf)     | Has details on I/O multiplexing, USB, and others                                                          |
| Vendor link                                   | [digikey](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)      | Digikey, Jameco, etc.  Do not paste links directly into the table.  Use a [link](#)                       |
| Code Examples                                 | [I2C](https://docs.espressif.com/projects/arduino-esp32/en/latest/api/i2c.html) [sensor tutorials](https://www.youtube.com/watch?v=M3YetBHXsaU)     | url(s) for libraries on github or other sites related to the microcontroller and your planned peripherals |
| External Resources URL(s)                     | [tutorial](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html) [tutorial](https://www.sunfounder.com/blogs/news/esp32-tutorial-a-comprehensive-guide-to-esp32-boards-features-and-getting-started?srsltid=AfmBOoq0Rigol8j_W6bblAoUfDbGW1UHGosg6gkVQ4yVkZkxZZP02yKS)      | Search on Google and YouTube for other resources for each specific microcontroller.                       |
| Unit cost                                     | $5.06      | Find on Digikey, Jameco, MPJA, or octopart                                                                |
| Absolute Maximum Current for entire IC        | 355mA      | Find in the microcontroller datasheet                                                                     |
| Supply Voltage Range                          | 3.0V, 3.3V, and 3.6V    | Min / Nominal / Max / Absolute Max, as found in datasheet                                                 |
| Absolute Maximum current <br> (for entire IC) | 355mA      | as found in datasheet                                                                                     |
| Maximum GPIO current <br> (per pin)           | 40mA      | as found in datasheet                                                                                     |
| Supports External Interrupts?                 | Yes      | as found in datasheet                                                                                     |
| Required Programming Hardware, Cost, URL      | The ESP32 an be programmed with the SNAP from MPLAB, which is $11.21 per unit, [URL](https://www.digikey.com/en/products/detail/microchip-technology/PG164100/9562532?gclsrc=aw.ds&gad_source=1&gad_campaignid=20790518593&gclid=Cj0KCQiA7rDMBhCjARIsAGDBuEBFDBDZAXSOk26tpPlg5tqYGxDdNkjizXdNqGZbL3J6GM2AoDbkyekaAsYEEALw_wcB)      | as found in datasheet                                                                                     |

| Module         | # Available | Needed | Associated Pins (or * for any) |
| -------------- | ----------- | ------ | ------------------------------ |
| UART           | 3           | 2      | *                              |
| external SPI\* | 4           | 0      | *                              |
| I2C            | 2           | 2      | *                              |
| GPIO           | 36          | 2      | *                              |
| ADC            | 20          | 0      | IO1, IO2, IO3, IO4, IO5, IO6, IO7, IO8, IO9, IO10, IO11, IO12. IO13, IO14, IO15, IO16, IO17, IO18, IO19, IO20                              |
| LED PWM        | 8           | 2      | *                              |
| Motor PWM      | 2           | 0      | *                              |
| USB Programmer | 0           | 0      | Will be programmed with the MPLAB Snap                              |

**Requirements:** For my board to work I need  1 UART and 1 IC2 subsytem. I also will need 2 GPIO pins. The total pins I will be using is 9, 2 UART, 2 I2C, 2 GPIO, 1 clock, 1 power and 1 ground.

**Role in Project:** My role in my group is to create a PCB to monitor and record the ambient temperature to the user interface.

![](Esp32.png)

**Pin Assignments:**
|Peripheral|Pins|: |LED 1|GPIO 1, GND| |LED 2|GPIO 12, GND| |LED 3|GPIO 3, GND| |Temperature|IO 8-10, GND| |UART|IO 36-37|

**Microcontroller Selection:**
The esp32 beats out the pic in a multitude of ways. Memory, processing, storage, bluetooth and wifi. All of these I wont be needing except for the processing. The efficiency in processing information is much quicker leading to faster more accurate results with less hardware involved. Although the job could be done with either, I am cleary favoring working with the esp32.

