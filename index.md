
Welcome the Red Salt Games Tombstone engine site where you can find examples, tutorials, hints and tips about the Tombstone games engine. We plan to regularly update this website as we generate interesting content regarding creating games with Tombstone.

Disclaimer: This is an unofficial site and we are not affiliated with Terathon software, creator of the Tombstone games engine.

## How a game is made using Tombstone
The Tombstone engine separates the development process into two major workflows. The first that relates to programming side and is performed by coding your game in C++, while the second relates to generating content (your game world, objects, their position in space, their materials, etc. ), using Tombstone's World Editor and relevant tools. 

When the program of your game starts, it will parse a world (i.e. a part of your game for example a level), and through the functions you have defined, will perform some initialization actions. These actions may for example be building a list of enemies for later use, or deciding where to spawn the player. Your program will be able to infer various characteristics through Tombstone's various classes and its class inference mechanicsm. 

The rest of the game logic is then left to be handled by the engine that again calls member functions of certain objects. Central to this logic is Tombstone's "controller" classes, that are responsible for controlling the behaviour of a game object. For example a controller may be responsible for the motion of an axe (and the programmer will code in how it behaves using C++), or another controller may be responsible for the colour change on a Halo effect and so on.

