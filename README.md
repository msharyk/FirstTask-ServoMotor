# FirstTask-ServoMotor
in this task i work with ARDUINO-UNo
then add 5 Servo motor 
make these 5 motors turn on 90 degres 


https://www.tinkercad.com/things/f4Aw0iLmmb3-epic-waasa-snaget/editel?sharecode=1uV32zOlOCZpDn74QVKoBBeGDRPa0UTPCQUt9lmM_aw




code:
// C++ code
//
/*
  Sweep

  by BARRAGAN <http://barraganstudio.com>
  This example code is in the public domain.

  modified 8 Nov 2013  by Scott Fitzgerald
  http://www.arduino.cc/en/Tutorial/Sweep
*/

#include <Servo.h>

int pos = 0;

Servo servo_9;

void setup()
{
  servo_9.attach(9, 500, 2500);

}

void loop()
{
  // sweep the servo from 0 to 180 degrees in steps
  // of 1 degrees
  for (pos = 0; pos <= 90; pos += 1) {
    // tell servo to go to position in variable 'pos'
    servo_9.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
  for (pos = 90; pos >= 0; pos -= 1) {
    // tell servo to go to position in variable 'pos'
    servo_9.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
}
