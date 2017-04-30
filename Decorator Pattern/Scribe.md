
Lets say we want to build an ordering system for a coffee shop that servers four kinds of beverages(House blend, Dark roast, Espresso, Decaf) with an option to add condiments to the beverage such as milk, soy, whip, mocha. The class diagram would look like

![screen shot 2017-04-30 at 11 49 37](https://cloud.githubusercontent.com/assets/17459420/25567089/2546af7e-2d9b-11e7-96b9-fd175797c93e.png)

We have an IS-A relationship between coffees and Beverage superclass. This looks like a simple design which can be extended to add other beverages easily in the future if required. 

What are we forgetting here? Variants of coffee with condiments. For example Dark Roast with milk or soy, DarkRoast with milk and mocha, Houseblend with mocha etc. To accomodate this we need to add more subclasses.

![screen shot 2017-04-30 at 12 02 57](https://cloud.githubusercontent.com/assets/17459420/25567181/ffabb62c-2d9c-11e7-8467-a79c9e15addc.png)

Result? Class Explosion!!!
The design is just not manageable and requires complex logic if new condiments and drink additions happen.

This brings us to 
Desing Principle #5: Classes should be open for extension and closed for modification
The goal is to have designs that we can augment at any time, but do it without touching the current code.

Decorator Pattern provides a flexible alternative to subclassing for extending functionality. Decorator class diagram is as shown below.

![screen shot 2017-04-30 at 12 20 28](https://cloud.githubusercontent.com/assets/17459420/25567314/959f34b8-2d9f-11e7-8aa8-f6dc7bcf723e.png)

There are two important parts to Decorator pattern.
1. Components which are the beverages in our example and
2. Decorators which are the condiments in our example.

In the class diagram above, the component class is an interface or an abstract class that is implemented by the concrete components (different kinds of beverage in our example). The decorator class which is also often an abstract class also implements the component class. This is the important part of Decorator pattern. Concrete decorators implement decorator class. 

It is important for concrete components and decorators to implement the component superclass so that we can wrap any decorator around any of the components. For example, in the coffee shop example, we want to be able to wrap any of the condiments around any of the coffees, and then pull the cost and get description methods on any of these wrapped objects Or even an unwrapped object and get the correct result. 

Explantion will become more clear in the Coffee shop implementation provided in the Code folder.








