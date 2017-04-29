
Overuse of Inheritance can result in designs that are quite inflexible and not amenable to change.
To demonstrate the problems with inheritance lets follow the example below:

![screen shot 2017-04-28 at 19 59 59](https://cloud.githubusercontent.com/assets/17459420/25552581/8dc0854c-2c52-11e7-961d-34cb32f547f6.png)

Lets say we want to design a Duck simulator. Duck is an abstract class that has a quack method, swim method and an abstract display method(Describes the appearance of the duck). Mallard duck and Redhead duck are concrete classes which implement their respective display methods. The design looks good so far. Isn't it? 

Now lets say we get a request to add another duck, "Rubber duck". We have a slight problem now. Rubber ducks don't quack.They squeak. But this problem can be handled by overriding the quack method as shown below.

![screen shot 2017-04-29 at 10 56 58](https://cloud.githubusercontent.com/assets/17459420/25557666/cb41b81e-2cca-11e7-9be4-e44dcabca1cf.png)

Now what if get a request to add an aditional feature to say make ducks fly. We can leverage inheritance by adding fly method to super class 'duck'. But we all know Rubber ducks can't fly. So we need to fix rubber duck again by overriding the fly method as shown.

![screen shot 2017-04-29 at 11 04 38](https://cloud.githubusercontent.com/assets/17459420/25557714/c01565fc-2ccb-11e7-850c-ca76d0670103.png)

Lets say we add another duck "Decoy duck" into our design. Decoy ducks don't squeak, so we need to override quack method. They don't fly, so we need to override fly method as well. Now we see that we are overriding most of the methods from super class and we are not really benefitting from inheritance, atleast for this duck.

![screen shot 2017-04-29 at 11 14 55](https://cloud.githubusercontent.com/assets/17459420/25557775/2dd5e70a-2ccd-11e7-87fd-cc078d3a8ad9.png)

Problem with this Design ?
1. Although we are keeping ducks organized in a hierarchy of classes we don't seem to be getting any reuse benefits. We are duplicating the code across classes.
2. We can't look at our superclass and get a lot of direct knowledge of the ducks anymore. We realy have to go into each concrete class to understand more about what the code does.
3. As we saw with fly method. A simple change to superclass can lead to unintended side effects with the other ducks.
4. A major issue with this design is that all the behavior of the ducks is assigned at the compile time. So we cannot change particlular duck instance at run time.
So this design isn't actually giving us a lot of flexibility as we might have expected.

How about we use Interfaces you say? Let us rework our duck interfaces. Lets create two interfaces, flyable and quackable.

![screen shot 2017-04-29 at 12 12 25](https://cloud.githubusercontent.com/assets/17459420/25558139/301ad0fe-2cd5-11e7-8b98-0dfe1afc03b4.png)

Problem with this design you ask? 
1. If there are 20 or 30 ducks say, then each duck will have to implement its own fly and quack methods. Absolutely no advantage of code reuse.
2. Any changes needed to fly or quack methods would require one to look at the code at each of the classes and make changes. Worst maintenance nightmare.
3. Still doesn't provide for runtime changes to behaviors should we want to.










