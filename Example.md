Example of usage

# Details #
```
#include "bmp085.h"

bmp085 BMP085;


void setup()
{
  Serial.begin(9600);
  BMP085.Calibrate();
}

void loop()
{

    BMP085.refresh();
   
    Serial.print(BMP085.pressure);
    Serial.print(", ");
    Serial.println(BMP085.temperature);

    delay(5000);
}
```