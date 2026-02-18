---
title: Module's Selected Major Components
---

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
