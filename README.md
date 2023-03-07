# minecraft_project

This is a minecraft design project that you can start with kids.

Summary of the code:

This code uses the Ursina game engine library to create a simple interactive scene with a player character that can move around and interact with objects using the mouse.

The from ursina import * statement imports all the necessary functions and objects from the Ursina library.

The from ursina.prefabs.first_person_controller import FirstPersonController statement imports a ready-made object for creating a player character that can move around in a first-person perspective.

app = Ursina() creates the game/application object.

Sky() creates a default sky background for the scene.

player = FirstPersonController() creates the player character.

A list named boxes is created to store instances of the Button class, which will be used to create cube-shaped objects.

The for loop creates a 2D grid of 8x8 cubes by iterating over two nested ranges. Each cube is created using the Button class, with the model set to 'cube', origin_y set to 0.5 (so that the cube is resting on the ground), and position set to (k, 0, n) for each iteration. The Button class also takes in additional arguments to specify the texture, color, and highlight color of the cubes.

The input(key) function defines what happens when the left or right mouse button is pressed while hovering over one of the cubes. If the left mouse button is pressed, a new cube is created at the position of the cube currently being hovered over, using the same properties as the original cubes but with the position adjusted by the mouse normal. If the right mouse button is pressed, the original cube is removed from the boxes list and destroyed.

app.run() starts the game loop, which continuously updates the scene and checks for user input.
