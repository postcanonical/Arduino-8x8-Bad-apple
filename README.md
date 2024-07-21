# Bad Apple on Arduino 8x8 matrix
## How to use this repo

Use code in [Arduino folder](Arduino) for your Arduino UNO. I am using [PlatformIO](https://platformio.org/) as my IDE, you can use it too, or just use lib and [main.cpp](Arduino/src/main.cpp).

Use code in [Scripts folder](Scripts) to generate frames and pass them to your Arduino.

## How to use scripts

1. Use [ffmpeg.sh](Scripts/ffmpeg.sh) to create squred and scaled video and get `.pbm` frames from it. `.pbm` uses 0 and 1 to display black and white, that is what we need.
1. Use [conv-to-bin-data-header.cpp](Scripts/conv-to-bin-data-header.cpp) to convert frames into C++ data header, it will create [data.h](Scripts/data.h).
1. Use [conv-to-decimal.cpp](Scripts/conv-to-decimal.cpp) to convert this data into decimal and store it in frames.csv.
1. Use [output-to-Serial.py](Scripts/output-to-Serial.py) to output frames.csv into the serial port of your Arduino and start VLC with BadApple video

## Video

[YouTube](https://youtu.be/mr9ofB3T-zI?si=xS27Of0pP8aEbBwd)