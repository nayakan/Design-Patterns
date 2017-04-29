
Overuse of Inheritance can result in designs that are quite inflexible and not amenable to change.
To demonstrate the problems with inheritance lets follow the example below:

![screen shot 2017-04-28 at 19 59 59](https://cloud.githubusercontent.com/assets/17459420/25552581/8dc0854c-2c52-11e7-961d-34cb32f547f6.png)

Lets say we want to design a Duck simulator. Duck is an abstract class that has a quack method, swim method and an abstract display method. Mallard duck and Redhead duck are concrete classes which implement their respective display methods.

