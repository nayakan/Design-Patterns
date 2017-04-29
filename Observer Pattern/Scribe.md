Observer pattern: A one to many dependency between objects (Subjects and dependents) so that when one object changes state, all of its dependents are notified and updated automatically.

![screen shot 2017-04-29 at 15 55 09](https://cloud.githubusercontent.com/assets/17459420/25559663/4bec5c48-2cf4-11e7-89ff-ea62758018b1.png)

Dependent here means that these objects are dependent on subject for data. Dependents are often called as observers as dependents observe the subejct.

Subject here is the sole owner of copy of data. This provides for a cleaner design than many object's owning the same data.

Class Diagram for a Observer pattern is as shown. We are showing only one observer here but the subject in general have many observers.

![screen shot 2017-04-29 at 16 09 40](https://cloud.githubusercontent.com/assets/17459420/25559773/4ef41780-2cf6-11e7-87ff-c0e5ef6ac156.png)

The subject interface has two methods that allow dependents to register or remove themselves from observing the subject. It also includes a notifyObserver method.
The Observer interface has only one method, update. That's what the subject calls to tell the dependents that data in the subject has changed. The ConcreteSubject implements the notifyObserver method, which is called any time data changes. And this method calls the update method on each observer. 

To illustrate Observer Pattern please look at the class diagram below for a Weather Station:

![screen shot 2017-04-29 at 16 26 12](https://cloud.githubusercontent.com/assets/17459420/25559848/9e496d74-2cf8-11e7-8c79-1a344ace0892.png)



