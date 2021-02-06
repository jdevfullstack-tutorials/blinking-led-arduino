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

![design](res/src1.png)


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
There are just 3 commands here:

`pinMode` is the command you tell the Arduino
board what is the mode of a particular pin.
If ever you did not mention that, then the
default is `input`.

`digitalWrite` is the command whether
there will be supply of voltage `HIGH`
or there is none `LOW` for a particular
pin, like in our example,
Arduino Digital Pin 13. For a basic LED,
we all know that when there is sufficient
voltage, it will light up and if there
is none, there will be none.

`delay` is the command for temporarily delay
a program, just like a pause. If prior to 
this, an LED is light up, it will pause for 
a certain amount of time with the initial 
status of the LED. It's in terms of milliseconds,
because for computers, they work in terms of
milli or nanoseconds. For example, they can 
accomplish 1000 digital task in just 1 second.
For high-powered servers, it's more than that.
For advanced programmers, this is very critical:
it can be used for multi-tasking, that 1 second
delay can be used by another mini-program.
