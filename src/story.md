# Detailed STEP by STEP workflow of the group project "The Arm-y"


## An exciting start: --------------------------- Edward Moriarty's Meeting
 On our first day at the Hope afternoon meeting (23/10/2024), we were greeted by Ed and a team of Italian tutors who helped us get everything started and decide which projects were worth the effort. After setting up our initial groups (based on everyone’s preferences), Ed himself, and sometimes even other people from the MIT Institute, started talking to each group on different occasions (both in person and via calls) to share his experience and thoughts on what he believed was the correct course of action for the things we wanted to make. They would often provide us with extremely valuable information to pursue something that was actually feasible with our resources—essentially making sure we wouldn’t waste any time or money.

## The First Ideas -------------- Brainstorm Phase
 The first thing we did was organise exactly what we needed to figure out and in what order. Since our final objective was to create a robotic 3D-printed arm that could be controlled wirelessly, we immediately began searching for a suitable 3D model of the arm and also started learning the basics of Arduino, as not everyone was already an expert in this regard.
After that, we:
·	Set up a **_GitHub repository_** for everyone to collaborate more efficiently.
·	Conducted numerous tests on the connection side of things (all of which are available on GitHub!) and, around the Christmas period, decided to use Arduino Cloud for the connections between boards.
·	Printed all the necessary 3D parts with standard PLA filament and adjusted some of them to our needs using Blender (such as connecting the three fingers together for a stronger grip, an idea that originated from Ed).
·	Assembled the parts and installed our first servo-motors (the actual moving parts behind the fingers).
·	Programmed the base to make the servo-motors respond to manual input.
·	Searched for a way to integrate Arduino with brainwaves (since we initially wanted to translate those waves into movements).

## The Intermediate Work Phase
 With the project's foundations now in place, we felt ready to take a step forward and purchase the necessary sensor to use brainwaves within the Arduino environment. The problem was, aside from being terribly expensive, this sensor had practically no documentation and had received many negative reviews for its fragility. However, it was still the only remotely usable option for the project... but with limited resources and with us not being able to risk spending all that money on a crucial component of dubious quality, we consulted with each other to decide whether to change direction and opt for a simpler control system that could be created in less time or not. We settled to use a glove filled with flex sensors connected to an Arduino board, which would send all inputs to the cloud, set up to be dynamically used by the robotic arm to move all its parts.
 To test the new method, we programmed the second board, identified as "glove", and initially connected just one flex sensor to check if it worked properly. From this test, it quickly became apparent that our flex sensors were deteriorating too easily and giving inaccurate readings, resulting in movements of the arm that were misaligned with the actual movement. Knowing this, we had two options:
1.	Search for significantly higher-quality flex sensors, which would increase the total cost of the project.
2.	Change the method of movement measuring with something else.
 Meanwhile, thanks to our personal 3D printer (the school’s one had unfortunately broken), we completed and assembled all the parts of the arm, including the internal servo-motors, the joint for a potential shoulder, the three joined fingers, internal wires, the external casing, and the internal board responsible for controlling all the servo and mini servo-motors.
 Apart from a few other modifications we still needed to make later on an aesthetic level, the arm itself was considered practically finished since we had already completed all the programming. Now, we had to start thinking again about how we wanted the user to control its movement.
 By the end of January (2025), Ed’s team returned to assist all the groups at the institute. Taking advantage of this opportunity, we asked the experts for a more efficient way to obtain numerical values from the glove’s movement (thus discarding the flex sensors). In response, Ed redirected us to the YouTube channel of Lucas Pope, a genius who had managed to create very cheap virtual reality gloves. By researching his project and, most importantly, observing the design of his gloves, we realised that all we needed were simple potentiometers and some wires.
 We took the potentiometers, attached them to the glove and its board, and finally completed the control system. All that was left was to test everything thoroughly and refine the final product, at least for the robotic arm itself. Naturally, we also needed to finish the wiki website hosted on github.

## Testing Phase and Finalisation
 Once we had a fully functional arm and the first prototype of the glove with the potentiometers, we tried to move the first finger completely wirelessly. In front of our professors and friends, who were anxiously waiting to see this promised remote-controlled arm, we managed to move the ring finger in real-time without any issues or significant delays. We had achieved our goal!
 From that moment on, we dedicated all our subsequent meetings to perfecting and adding extra features, such as the mobile app to control the arm via Bluetooth (still in development), or improving the design of our project's wiki website.
 We will do our best to improve our product as much as possible, starting with getting the entire hand to move smoothly! And maybe we’ll even think about making the design a bit more appealing, since right now it looks more like a Frankenstein creation made of hot glue, plastic, rope, and circuits. But that’s another story that we will fix later.

