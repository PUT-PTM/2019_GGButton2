# 2019_GGButton2

### Overview

Wav player created on STM32 Microcontroller(STM32F407VG). Delight yourself listening to great music. 

### Description

Wav files are stored on SD card, there is no limit in the number of songs, but keep in mind that every WAV needs to be in 8 audio bitdepth, 16 kHZ sample frequency and mono channel. Also song name needs to end .WAV ( lowercase won't work). GGButton usage couldn't be easier: 
 - pressing button once plays the song, pressing it again will stop, press third time to resume
 - to change volume use the potentiometer ( first winder from the right)
 - to change song use the encoder ( second winder from the right)
 - display's first line shows currenly chosen song
 - display's second line shows the volume level

### Tools

 - System Workbench for STM32
 - STM32 CubeMX

### How to run

#### Hardware:
 - STM32f4-DISCOVERY board,
 - SD Card Module and SD Card formatted to FAT32,
 - 1 potentiometer
 - 1 encoder
 - 1 LCD 16x2 
 - Headphones or speakers with male jack conncetor
#### Connection instruction
 - Encoder
    - VCC <---> 3V
    - GND <---> GND
    - SIB <---> PE11
    - SIA <---> PE9
 - Button
    - VCC <---> 3V
    - GPIO_EXTI <---> PB0
  - Potentiometer 
    - VCC <---> 3V
    - GND <---> GND
    - ADC <---> PA0
  - SD Module
    - MOSI <---> PB5
    - MISO <---> PB4
    - SCK <--->PB3
    - VCC <---> 5V
    - GND <---> GND
    - CS <---> GND
  - LCD
    - VDD <---> 5V
    - VSS <---> GND
    - VO <---> PA5
    - RS <---> PE0
    - RW <---> GND
    - E <---> PE1
    - D4 <---> PD8
    - D5 <---> PD9
    - D6 <---> PD10
    - D7 <---> PD11
    - A <---> 3V
    - K <---> GND

#### How to run
Using STMCubeMX run the i2s.ioc file, then just simply press "Generate project' button. New window will pop up, click open project and compile it. 

### Future improvements

We would like to improve the project by enhancing the sound quality by using not mono but stereo sound. Also we feel that GGButton's display is missing moving song title, when it has more than 13 characters. 

### Attributions

http://elm-chan.org/fsw/ff/00index_e.html

https://drive.google.com/file/d/1d1NUP34WZQnrs0Jo_9XTO_aFkIdpvjH0/view

https://drive.google.com/file/d/1owONAt5fz6kvUhxOB1KD2_UUCZI2uAXA/view


### Credits

Result of Jacek Eichler and David Solomon work 

The project was conducted during the Microprocessor Lab course held by the Institute of Control and Information Engineering, Poznan University of Technology.

Supervisor: Tomasz Mańkowski
