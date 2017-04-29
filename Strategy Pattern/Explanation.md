
Overuse of Inheritance can result in designs that are quite inflexible and not amenable to change.
To demonstrate the problems with inheritance lets follow the example below:

![screen shot 2017-04-28 at 19 59 59](https://cloud.githubusercontent.com/assets/17459420/25552581/8dc0854c-2c52-11e7-961d-34cb32f547f6.png)

Lets say we want to design a Duck simulator. Duck is an abstract class that has a quack method, swim method and an abstract display method(Describes the appearance of the duck). Mallard duck and Redhead duck are concrete classes which implement their respective display methods. The design looks good so far. Isn't it? 

Now lets say we get a request to add another duck, "Rubber duck". We have a slight problem now. Rubber ducks don't quack.They squeak. But this problem can be handled by overriding the quack method as shown below.

![screen shot 2017-04-29 at 10 56 58](https://cloud.githubusercontent.com/assets/17459420/25557666/cb41b81e-2cca-11e7-9be4-e44dcabca1cf.png)

Now what if get a request to add an aditional feature to say make ducks fly. We can leverage inheritance by adding fly method to super class 'duck'. But we all know Rubber ducks can't fly. So we need to fix rubber duck again by overriding the fly method as shown.

![screen shot 2017-04-29 at 11 04 38](https://cloud.githubusercontent.com/assets/17459420/25557714/c01565fc-2ccb-11e7-850c-ca76d0670103.png)





