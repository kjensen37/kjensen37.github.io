---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for  .....

### Power Management

(**remove this note/placeholder**: this is where your 3.3 volt switching regulator, any other needed power regulator, and power source {if applicable} **THAT WERE SELECTED**)

For more details, review the ["Appendix - Component Selection Process - Power Mangement"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#power-management) selection.

### Sensor

(**remove this note/placeholder**: if applicable, this is where your  **SELECTED** sensor is shown. Otherwise, remove this section.)

For more details, review the ["Appendix - Component Selection Process - Sensor"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#sensor) selection.

-----------

**Temperature Sensor**

1. IC TEMP SENSOR - TMP1075DSGR

    ![](temp1.png)

    * $0.46/each
    * [link to product](https://www.digikey.com/en/products/detail/texas-instruments/TMP1075DSGR/10715322)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Digital Output                             | I²C Required |
    | Good Accuracy & Resolution                      | Cost Slightly Higher                                        |
    | Low Power & Wide Supply                      | Longer Conversion Latency                                      |

   2. LOW-POWER HIGH-ACCURACY ANALOG O - TMP235A4DBZR

    ![](temp2.png)

    * $0.36/each
    * [link to product](https://www.digikey.com/en/products/detail/texas-instruments/TMP235A4DBZR/9649794)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Simple Analog Output                             | Analog Complexity |
    | Wide Operating Range                     | Moderate Accuracy                                      |
    | Low Quiescent Power                    |  Output Susceptible to Noise |

   3. SENSOR ANALOG -40C-125C SC70-5 - MCP9700T-E/LT

    ![](temp3.png)

    * $0.40/each
    * [link to product](https://www.digikey.com/en/products/detail/microchip-technology/MCP9700T-E-LT/735965)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Very Low Cost & Easy                              | Lower Accuracy|
    | Direct ADC Readout                   | No Digital Interface                                       |
    | Low Power Consumption                  | Readings Affected by System |

**Rationale:** I have chosen option #1, the TMP1075DSGR temperature sensor. Although it is the most expensive of the three, the use of I2C will be beneficial aswell as the accuracy and a 12-bit resolution. I believe that the ease of use aswell as the accuracy are enough for me to choose it even with the cost difference.

---------------------

**3.3 Volt Switching Regulator**

1. IC REG BUCK 3.3V 1.5A SOT23-5 - SC189ZSKTRT

    ![](reg1.png)

    * $0.86/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | High efficiency step-down design                               |Limited output current|
    | Small footprint                     | Fixed output only                                     |
    | Wide input range | No advanced features |

   2. IC REG BOOST ADJ 980MA SOT23-6 - TLV61046ADBVR

    ![](reg2.png)

    * $1.24/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Boost capability                             | Not a true linear regulator |
    | Integrated protections                   | Boost only                                       |
    | Isolation in shutdown                    |Current limits dependent on configuration |

   3. IC REG BUCK 3.3V 2A TSOT23-6 - AP63203WU-7

    ![](reg3.png)

    * $0.71/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Higher output current (2 A)                             | Fixed output |
    | Wide input range                     | Requires external inductors/caps                                      |
    | EMI-friendly design | Higher complexity vs LDO |

**Rationale:** The voltage regulator I am choosing is #1, the SC189ZSKTRT. The reason being the small footprint for more real estate on the pcb and I think when it comes to a voltage regulator atleast for the scope of my PCB functions, no advanced features are more of pro than a con for simplicity.

---------------------

**LED**

1. LED ORANGE CLEAR CHIP SMD - LTST-C190KFKT

    ![](led1.png)

    * $0.86/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Very Small & Low-cost                       | Limited Brightness|
    | Low Power Consumption                    | Single Color Only                                      |
    | Easy to Integrate | Wide Viewing Angle but Basic Performance |

   2. LED RGB 0404 SMD - UHD111A-FKA-C3K23E1L3VG5ZB3Z3

    ![](led2.png)

    * $1.24/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Full RGB Control                             | Complex Drive Requirements |
    | Compact & Bright for Size                  | Lower Output vs High-Power LEDs                                     |
    | Good for Dynamic Displays | Moisture Sensitivity |

   3. LED RED DIFFUSED 1608 SMD - SML-D12U1WT86

    ![](led3.png)

    * $0.71/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Compact Footprint                             | Single Color Only |
    | Good Visibility                   | Limited Application Beyond Indicators                                     |
    | Standard Drive Requirements| Mid-Level Brightness |

**Rationale:** The LED I will be using is #1, the LTST-C190KFKT. Simplicity yet again showing favoritism, as being just debugging LED's, there is no need for overcomplexity nor high spending. The cheapest and simplest of these three is #1.

---------------------------------

**Microcontroller Selection**

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
| UART           | ?           | ?      | ?                              |
| external SPI\* | ?           | ?      | ?                              |
| I2C            | ?           | ?      | ?                              |
| GPIO           | ?           | ?      | ?                              |
| ADC            | ?           | ?      | ?                              |
| LED PWM        | ?           | ?      | ?                              |
| Motor PWM      | ?           | ?      | ?                              |
| USB Programmer | ?           | 1      | ?                              |
| ...            |



\* The ESP32-S2 has multiple SPI interfaces, but some are for internal use
