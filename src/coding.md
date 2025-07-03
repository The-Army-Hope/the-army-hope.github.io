# ALL CODING RELATED INFORMATIONS OF THIS PROJECT
Below are some coding notes and considerations.<br>
If you would like to look at the whole project files and more, you can visit our GitHub [organization](https://github.com/The-Army-Hope) and our [main project repository](https://github.com/The-Army-Hope/RemoteArm) where everything related to Remote Arm project (coding related and more) is saved and documented.<br>
I'd suggest to also take a look at [all the tests I made](https://github.com/The-Army-Hope/Arduino-Tests) before starting with the arm project directly, just to get known with Arduino better; trust me some of them were really cool to look at!

## Splitting the work
As we said before, we divided the coding tasks into 2:

| Physical coding team                                                                    | Connection / Cloud coding team            |
| --------------------------------------------------------------------------------------- | ----------------------------------------- |
| [Matte549](https://github.com/Matte549) and [Turkiztron](https://github.com/turkiz-jpg) | [NexIsDumb](https://github.com/NexIsDumb) |

The _Physical coding team_ would have worked on the physical base (like fingers movements), the _Connection / Cloud coding team_ would have worked on figuring out the best way to connect remotely the two Arduinos and also code it.

As the physical base group proceeded, the connection team instead thought at first to buy a server and a domain to make the two boards communicate, it wasn't hard to code either but issues like "what would happen if you stopped paying yearly for the server" popped up: if we wanted something to be working forever we had to find another way.<br>
While searching online we found out about Arduino Cloud and it being free and compatible with our R4 boards.<br>
After the connection ran some tests to understand how it worked, they immediately understood that it was the best option.

## How it developed
As the physical base group started using the servos and flex libraries to complete it whole, the connection team made two _Arduino Could "Things"_; the _Glove Thing_ and the _Arm Thing_ and linked the two arduinos to them, using at first a single sycnhronized variable that was a string containing all the needed finger and body parts movement degrees splitted by a comma through a specific split code: at first they thought this would make it faster to send since they were less Bits, the arm would split and get the right values out of the string.<br>
Although after a while they realized that it was annoying understanding on which position of the string were the right degree values of each arm part and that using multiple integrer values wouldn't made the project lag at all and so they went for that way.

## How it ended
Once every group finished their coding part, [NexIsDumb](https://github.com/NexIsDumb) started merging everything together and separating the right way the Arm and Glove code and optimize it too a little bit. With [Matte549](https://github.com/Matte549)'s help they also started to find the right finger max and min values for making it work best.<br>
The final big showcase and test of the project was made at [NexIsDumb](https://github.com/NexIsDumb)'s finals: during the last exam he started moving with [Matte549](https://github.com/Matte549)'s help the arm perfectly fine through the glove and all professors were completely amazed!<br>
Unfortunately we couldn't make it in time to add the palm, elbow and wrist, but they aren't hard to add since the code for them is already there.

## More coding notes
For getting the flex sensors and potentiometers values, the glove's code uses an `analogRead` function to get from the desired pin a value between 0 and 1023. To make sure this number was translated into integrer angles, we've used a `map` function setting specific min and max of the angles (that the program would have used based on `analogRead`'s raw number) based on how we've placed the servomotors in the arm, this took bunch of tries as you have to look on their position and rotation.<br>
Here's an example:
```ino
indexDeg = map(analogRead(indexPin), 0, 1023, 0, 180);  // From 0 to 1023, the raw number will be translated to: 0 to 180
```

Also during revisions, [NexIsDumb](https://github.com/NexIsDumb) felt better with using constants on some specific stuff like pin positions, for example:
```ino
const int potPinPollice = A1;  // Analogic thumb A1 pin connected to the potentiometer
```

Before we deleted the splitting string method, this was the split string function made by [NexIsDumb](https://github.com/NexIsDumb) (it was probably not perfect since it used dynamic memory, but was still cool to see it in action, probably using `char*` (aka _C strings_) would have been better):
```ino
const int MAX_RECEIVED_DEGREES = 5;

/*
  Splits a string with commas into an array of ints, for example "125,65,34" => [125,65,34]
*/
void getDegreesFromString(int degs[MAX_RECEIVED_DEGREES], String infos, char delim = ',') {
  int t = 0, r = 0, i;
  for (i = 0; i < infos.length() + 1 && t < MAX_RECEIVED_DEGREES; i++) if (infos[i] == delim || i == infos.length()) {
    if (i - r > 1) {
      degs[t] = infos.substring(r, i).toInt();
      t++;
    }
    r = i + 1;
  }
}
```

## A little consideration
This demonstrates that even something so easy to code can become something really cool, perfect ending and perfect prototype for a school project, HAH!<br>
\- Nex