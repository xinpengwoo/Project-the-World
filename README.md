@ Source: https://sp21.datastructur.es/materials/lab/lab12/lab12, https://sp21.datastructur.es/materials/proj/proj3/proj3, https://sp21.datastructur.es/materials/lab/lab13/lab13
@ Game example: https://sites.google.com/site/broguegame/, http://www.bay12games.com/dwarves/


```
├── Core
│   ├── Engine.java //Contains the two methods that allow interacting with your system.
│   ├── Main.java //How the user starts the entire system. Reads command line arguments and
|   |               calls the appropriate function in Engine.java.
│   └── RandomUtils.java //Handy utility methods for doing randomness related things.
├── InputDemo
│   ├── DemoInputSource.java
│   ├── InputSource.java
│   ├── KeyboardInputSource.java
│   ├── RandomInputSource.java
│   └── StringInputDevice.java
├── lab12
│   ├── BoringWorldDemo.java
│   ├── HexWorld.java
│   ├── project3prep.md
│   └── RandomWorldDemo.java
├── lab13
│   └── MemoryGame.java
├── Networking
│   ├── BYOWClient.java
│   └── BYOWServer.java
└── TileEngine
    ├── TERenderer.java //contains rendering-related methods.
    ├── TETile.java //the type used for representing tiles in the world.
    └── Tileset.java // a library of provided tiles.
```



`byow.Core.Engine` provides two methods for interacting with your system. The first is `public TETile[][] interactWithInputString(String input)`. This method takes as input a series of keyboard inputs, and returns a 2D `TETile` array representing the state of the universe after processing all the key presses provided in input (described below). The second is `public void interactWithKeyboard()`. This method takes input from the keyboard, and draws the result of each keypress to the screen. Lab 12 covers how to render tiles, and Lab 13 covers how to get user input.

This project makes heavy use of `StdDraw`, which is a package that has basic graphics rendering capabilities. Additionally, it supports user interaction with keyboard and mouse clicks. You will likely need to consult the API specification for `StdDraw` at some points in the project, which can be found [here](https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdDraw.html).