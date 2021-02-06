# Blinking LED Arduino
This is a blinking LED activity as the intro for 
Arduino Code programming.

## The Arduino Code
Arduino is both software and hardware. Right there,
you can control the design.

There are two built-in functions in Arduino Code:
`void setup` and `void loop`.

`void setup` is where you tell the computer whether
an electronic component being programmed is an
output device. Other initial setup can be
done here, like, the initial mode of an LED
is turned on.

`void loop` is where the execution of programs
happen.

Take note of the word `void`. A `void` type 
of function will simply execute all the commands
and will not return any value. Other functions
which are not void can return values.

## The Setup
You need an 3 basic LEDs, 1 breadboard and
the Arduino UNO board.

Follow the wiring as indicated in the picture
below:


Then, go to `Code` section and copy the initial
code below:

```
void setup()
{
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
}

void loop()
{
  digitalWrite(13, HIGH);
  digitalWrite(12, LOW);
  digitalWrite(11, LOW);
  delay(1000);
  
  digitalWrite(13, LOW);
  digitalWrite(12, HIGH);
  digitalWrite(11, LOW);
  delay(1000);
  
  digitalWrite(13, LOW);
  digitalWrite(12, LOW);
  digitalWrite(11, HIGH);
  delay(1000);
}
```

### Code Explanation

