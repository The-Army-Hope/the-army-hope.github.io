# WARNING
This is still a WIP website...<br>
(_TODO_: add the various team pages so they can write more, NOT on this page)

# What is the "The Army" project?
The Army is a school project born out of the _HoPE_ (_Hands on Physics Experience_) initiative, proposed by our school in collaboration with the _Massachusetts Institute of Technology_ (_MIT_). The goal of the project is to develop a mechanical arm that can be remotely controlled over long distances via an internet connection.

## Planning
After brainstorming basic ideas, we decided to adapt an old school project, which consisted of a simple motorized gripper, into something much more functional: a complete arm, including an elbow, entirely based on Arduino and its ecosystem. The addition of _Arduino Cloud_ allows communication between the controls and the arm, even across entire continents, and also _Smart Home_ integrations like _Alexa_ or _Google Home_.

Our six-person team divided the main tasks in:
- Communication
- 3D Modeling
- Assembly
- Programming

In every parts of the project the different teams interacted and some of them even helped the other by just for example even optimizing their codes.

## Gathering Resources for the Initial Sketch
The 3D modeling team immediately began searching for a base model to work from, finding it at https://www.thingiverse.com/thing:2269115. Meanwhile, the communication team researched how to use Arduino Cloud and collaborated with the programming team to transmit initial inputs through Arduino Cloud. This enabled the physical movement of servo motors provided by school funds.

## Developing the First Prototype
Using the school's 3D printer, the modeling team completed the printing of all essential parts, enabling the assembly team to begin their work. Compared to the original model, some parts were refined and modified using Blender. Notably, the last 3D-printed parts were combined to improve grip strength.<br>
The communication and programming teams wrote the necessary code for data transmission between two Arduinos connected via Arduino Cloud. They also implemented the code required to input passwords, allowing the Arduinos to connect to Wi-Fi.

## First Tests
Besides all the test ran by the project [here](https://github.com/The-Army-Hope/Arduino-Tests) the communication and programming teams, during a school celebration event, were able to run the first tests and show it off to their professors, and it actually started working (NOTE: The repository will stay private temp for now)!<br>
The tests were simple: since at the time we didn't have long cables or breadboards we could move only one finger per time.. and the index finger worked! Across the room the two teams started moving the finger through a potentiometer.

## Next steps
We'll try to separate one of the 3 fingers that were merged together, finalize the glove that should move the arm and finish this documentation website.