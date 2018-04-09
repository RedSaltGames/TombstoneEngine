# The Unofficial Tombstone Engine Website

Welcome the Red Salt Games Tombstone engine site where you can find examples, tutorials, hints and tips about the Tombstone games engine. We plan to regularly update this website as we generate interesting content regarding creating games with Tombstone.

Disclaimer: This is an unofficial site and we are not affiliated with Terathon software, creator of the Tombstone games engine.

## How a game is made using Tombstone : A brief and by no means complete excerpt
The Tombstone engine separates the development process into two major workflows. The first that relates to the programming side and is performed by coding your game in C++, while the second relates to generating content (your game world, objects, their position in space, their materials, etc. ), using Tombstone's World Editor and relevant tools. 

When the program of your game starts, it will parse a world (i.e. a part of your game for example a level), and through the functions you have defined, will perform some initialization actions. These actions may for example be building a list of enemies for later use, or deciding where to spawn the player. Your program will be able to infer various characteristics through Tombstone's various classes and its class inference mechanism. 

The rest of the game logic is then managed by the engine but by calling functions that the programmer has defined (mainly through deriving from some base classes). Central to this approach is Tombstone's "controller" classes, that are responsible for controlling the behavior of a game object. For example a controller may be responsible for the motion of an axe (and the programmer will code in how it behaves using C++), or another controller may be responsible for the color change on a Halo effect.

The controllers and other classes that are programmed in your game module (technically the module is a shared library), can be made available to the World Editor, through the definition of certain member functions. This will allow a level designer to assign through the World Editor the Halo Effect to certain nodes, or define the axe motion controller to an axe.

This creates the following workflow for the Tombstone engine:
1. First decide about the behavior of an object in your world.
2. Then subclass the controller class and program in the behavior. Also define appropriate member functions that can be used by the World Editor to display information to the level designer.
3. The level designer then uses the newly available controller to design the level in the World Editor.

Although we referred to just the Tombstone "controller" class, there are many more classes that will need to be sublclassed during the development of a game to achieve certain behaviors. Many of these are demonstrated in the examples we have prepared.
