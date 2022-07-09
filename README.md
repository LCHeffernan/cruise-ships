# Cruise ship.
___
This was my second JavaScript project, which was tested using Jest, the tests can be found in the \_\_tests__ folder. I created a GUI for this project which is in a different repo [here](https://github.com/LCHeffernan/cruise-ships-gui).

Ports are created which the ship can sail from and dock. These ports are then used to create an itinerary which is used by the ship.
___
## Download.
This project has the following dependencies: JavaScript, Jest and Node. To download the project:
* Fork the repository.
* Clone down your fork using ```git clone```.
* Change directory into your cloned folder and run ``` npm install ```.
* You can run the program in node REPL using the command ```node```.

To make the program available in REPL, type
* ```const Port = require("./src/port");```
* ```const Itinerary = require("./src/itinerary");```
* ```const Ship = require("./src/cruise-ship");```

Don't exit from REPL as this is where the program will be run.
___
## How to use:
Firstly you will need to create as many ports as you want (I have created 3), and an itinerary and ship. You can call your variables (ports, itinerary and ship anything you like).
* ```const dover = new Port('Dover');```
* ```const calais = new Port('Calais');```
* ```const oslo = new Port('Oslo');```
* ```const itinerary = new Itinerary([dover, calais, oslo]);```
* ```const neptune = new Ship(itinerary);```
Once you have these set up you can see which port the ship is currently at using ```neptune.currentPort.name``` (it should say Dover). You can sail to the next port using ```neptune.setSail();``` and then dock using ```neptune.dock();```. If you check the ship's current port using ```neptune.currentPort.name``` you can see it has changed to Calais. The previous port can be checked using ```neptune.previousPort.name``` which should now be Dover. If you continue to set sail and dock through the ports in the itinerary you will see the previous and current ports change. If you try to sail past the last port an error will be thrown saying "end of itinerary".
___
## Author.
Lisa Heffernan

* Twitter [@Iisaheffernan](https://twitter.com/Iisaheffernan)
* GitHub [@LCHeffernan](https://github.com/LCHeffernan)
* LinkedIn [Lisa Heffernan](https://www.linkedin.com/in/lisa-heffernan-54b61312a)
