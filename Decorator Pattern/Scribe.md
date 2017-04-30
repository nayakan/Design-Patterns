
Lets say we want to build an ordering system for a coffee shop that servers four kinds of beverages(House blend, Dark roast, Espresso, Decaf) with an option to add condiments to the beverage such as milk, soy, whip, mocha. The class diagram would look like

![screen shot 2017-04-30 at 11 49 37](https://cloud.githubusercontent.com/assets/17459420/25567089/2546af7e-2d9b-11e7-96b9-fd175797c93e.png)

We have an IS-A relationship between coffees and Beverage superclass. This looks like a simple design which can be extended to add other beverages easily in the future if required. 

What are we forgetting here? Variants of coffee with condiments. For example Dark Roast with milk or soy, DarkRoast with milk and mocha, Houseblend with mocha etc. To accomodate this we need to add more subclasses.

![screen shot 2017-04-30 at 12 02 57](https://cloud.githubusercontent.com/assets/17459420/25567181/ffabb62c-2d9c-11e7-8467-a79c9e15addc.png)

Result? Class Explosion!!!






