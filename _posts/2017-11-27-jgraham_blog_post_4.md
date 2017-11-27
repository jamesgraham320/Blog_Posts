---
layout: post
title:  "Javascript orbject relations refresher"
date:   2017-11-27
---

Object relations in javascript
------------------------------

Coming from ruby on rails, object relations are a breeze. Activerecord has macros to save you from all but the most convoluted relations you can think of. Javascript is a functional language with some object oriented thrown in. Basically this means that we are unfortunate enough to have to build this ourselves. Before we start creating relations in our classes and objects, we have to make all of our instances available in a global scope. Javascript doesn't have static variables so we have to create a global variable to hold all of our objects. Conventionally this is called 'store' but can really be called anything. We will also need global variables to keep track of the id's of all our objects. It looks like this:

![object store](https://image.ibb.co/g0MCk6/Screen_Shot_2017_11_27_at_10_59_25_AM.png)

Now that you've created a place to store all our objects and keep track of their id's it's time to create our object models. Here we're going to be modelling a has many through relationship with taxi drivers and their passengers. Drivers will have many passengers and vice versa, however for this to work we will need a join table in the form of trips. Starting with the Driver class:

![driver class](https://image.ibb.co/d5s4Xm/Screen_Shot_2017_11_27_at_11_04_28_AM.png)

This is a basic class to represent someone driving a taxi. They have a name and an id. Whenever a new one is created, it is added to the store so it can be found later. This saves us the hassle of naming them each individually. After creating the driver class, we can create passengers, which are largely teh same as drivers.

![passenger class](https://image.ibb.co/h3Jdsm/Screen_Shot_2017_11_27_at_11_04_56_AM.png)

Drivers and passengers both have methods to access the trips and drivers/passengers associated with them but without the trip class, its all meaningless. In our model, drivers have many trips and passengers have many trips. Whenever one class has many of another, one of them has to have an id so it knows who it belogns to. In our case, trips have to have passengerId and driverId so that we know who they belong to. Lets make that now:

![trips class](https://image.ibb.co/mYa2JR/Screen_Shot_2017_11_27_at_11_04_43_AM.png)

Great! Now that we have all of our classes we can talk about our accessor methods. Lets take a look at the Trip class. It has a passenger() and driver() method to access the objects that the trip belongs to. Basically we look into our store and use the iterator 'find' to compare the passengerId or driverId of the trip to the ids of the objects in the store and return the one that matches.
This gets only slightly more complicated when it comes to drivers and passengers. If you look at the driver class, it has a method called trips(). This accesses the store and filters all of the trips based on the id of the driver you're looking at (this.id === trip.driverId). This returns an array of all the trips that belong to a particular driver. The same process can be repeated for passengers. 
The very last method we have to look at seems complicated but is in fact very simple. Simply access the method to return an array of the objects trips and you can iterate over them to return all of their drivers/passengers. 
