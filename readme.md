spacebrewTouchDesigner
==============

A [Spacebrew](https://github.com/Spacebrew/spacebrew) bridge for [Touchdesigner](https://www.derivative.ca/)

About Spacebrew  
===============  
Spacebrew is an open, dynamically re-routable software toolkit for choreographing interactive spaces. Or, in other words, a simple way to connect interactive things to one another. Every element you hook up to the system can subscribe to, and publish data feeds. Each data feed has a data type. There are three different data types supported by Spacebrew: boolean (true/false), number range (0-1023) or string (text). Once elements are set up, you can use a web based visual switchboard to connect or disconnect publishers and subscribers to each other.  
  
[Learn more about Spacebrew here.](http://docs.spacebrew.cc/) 

Info
=============== 
This example is based heavily off of the [pySpacebrew](https://github.com/Spacebrew/pySpacebrew) example.

Setting Up the Example
============== 

###Before you Get Started: Install Dependencies   
Before you get started you need to install the appropriate websockets library. There are many different ones out there, so make sure to get the one called `websocket-client`. [Here is a link to code repo for the `websocket-client` library](https://github.com/liris/websocket-client). The easiest way to install this library is using pip, python's package manager. If you have pip installed on your computer all you have to do is run the command below in the Terminal (or whichever other console app you prefer). Otherwise, follow the instructions on the `websocket-client` repo.  
  
```
pip install websocket-client
```

###Configure Python modules in TouchDesigner
When you open up TouchDesigner for the first time you also need to configure your Python Module Path. This path will depend on where your version of Python is installed the default on Windows is something like: `C:/Users/[username]/AppData/Local/Programs/Python/Python36-32/Lib/site-packages` To confirm it is the right folder make sure that the `websocket-client` folder is there. Once you've updated the path restart TouchDesigner for the changes to take effect.

Running the Example
==============

- Start a Spacebrew server so that we have something to connect to.
- Run the SimpleTester html file to have an example client to send data from
    - Be sure to include url query strings `?server=localhost&name=tester`
    - You should see the tester connect in the [Spacebrew admin](http://localhost:9000)
- Then open up SimpleExample/SimpleSpacebrew.toe

![Alt text](/screenshots/overview.png "TouchDesigner Example")

![Alt text](/screenshots/spacebrew_tox.png "Spacebrew Tox")