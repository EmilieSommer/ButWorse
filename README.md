# ButWorse
My But Worse (Unpacking)
But Worse
Emilie Sommer Freltoft

Overview of the Idea and Project Parts
My mini-project is a room decorating game inspired by the indie game Unpacking. In my game, players can move and rotate objects, just like in the original game. The goal is to place various items, such as furniture and decorative objects, within a bedroom. The game is under the genre Cozy games, and is meant to be relaxing and slow paced. I used an orthographic camera to mimic an isometric style in my 3D game, inspired by the original game’s 2D visuals.

Although I haven’t played the original Unpacking, I was inspired by its subtle storytelling. A key feature in the original game is how it reveals a narrative through the rooms you unpack, showcasing how an unseen character progresses through life. Inspired by this, I designed a 12 year old child’s room and tried to include items that told a story.

3.  Screenshot of the room and objects imported into blender 
The room includes personal objects like a diary with an entry, a photo of two friends, and a teddy bear. These items hint at the story of a girl who is moving away from her old home and friends, feeling sad about the change. 
When you finish the game and press the done button you receive a text from the unseen character's mom, which both serves to confirm that you meant to press the done button as well as making the UI elements a part of the narrative.

The game consists of a room which is a single joined object created by combining all static elements that the player cannot move, like the bed and table as they serve as spots where you can unpack objects. 
Colliders are placed on all surfaces where objects can be placed, such as tables, shelves, and floors, allowing objects to snap and align correctly when moved.
All interactive objects that players use to decorate the room are stored in a box located beside the room. When you click the box, the objects appear one by one. Each object can be rotated 90 degrees when clicked, and they will snap to allowed surfaces specified in the inspector, which prevents placement in locations where the objects do not fit.
Project Parts
Scripts:
Interactive Camera Script: Locks the camera to an isometric perspective and allows smooth panning around the room. The camera rotates around the room from 0 to -90 degrees only.
PlaceableObject Script: Handles object dragging, rotation (90 degrees on click), and snapping to valid surfaces.
ObjectsFromBox Script: Manages objects being released from a box sequentially, including scaling for specific items if required.
Animation Trigger Script: Plays animations, such as opening the lid of the box, when interacting with objects.
Reset Script: Reloads the scene to reset the game.

Objects in Scene:
Room: The room contains large furniture (tables, shelves) and surfaces for interaction.
Box and Objects: A box that holds objects, which are released one by one as the player clicks. 
Camera: The camera is positioned for an isometric view and follows specific constraints, only rotating  around the room 0 to -90 .
Materials and Lighting:
Material: Materials were all painted on in Nomad Sculpt 
Lighting: A point light is placed outside the window to mimic sunlight and environment lighting is set to a warm tone to create a cozy environment..
Physics and Collisions:
Colliders: Box colliders are placed on all surfaces to ensure objects snap to surfaces and detect mouse clicks.
GUI:
UI Elements: A simple title menu consisting of a button that takes you to the Room scene. Where the interface consists of a reset button that uses the same change scene script to reload the scene and a done button which sends you to the menu.
Animations:
Box Lid Animation: A simple animation of the  box lid that opens smoothly when clicked, revealing objects inside.


Time Schedule and References

I spent two evenings creating the room and all the decoration objects in a sculpting app called Nomad sculpt. I spent some time trying different room styles and what decor I should create. I then spent almost 2 days trying to export it into Unity with great difficulty as i had painted the objects in Nomad directly on the vertices without using a base or normal map, and this could be exported to Blender with no issue, but Unity couldn't read the vertex colors so they were grey every time i exported. The biggest issue was understanding why this issue occurred and how vertex paint was processed by the program. The solution was to bake all the textures in Blender but I had to do it over 50 times to get the settings right so half the mesh didn’t export with black bits. The UV mapping islands kept overlapping when using blenders, smart UV mapping funktion. That was the most difficult part. I then spent 2 evenings completing the game, implementing the game functionality.

Time Schedule
Task
Hours Spent approximately
Sculpting all assets
6 (2 evenings)
Exporting materials
12 (2 days)
Box Interaction Script
1
PlaceableObject Script
3
Room/Light  Setup
3
Animations (Lid Opening)
1
UI setup
1


References:
Tools:
I used GitHub Copilot for troubleshooting and improving sections of my scripts.
Music:
Music track: Flourish by Pufino
Source: https://freetouse.com/music
Background Music (Free)

Videos on baking and exporting from Blender/Nomad sculpt:
CG Learner (Director). (2023, February 3). Easiest way to bake PBR textures in Blender [Video recording]. https://www.youtube.com/watch?v=MaMUfJsC92M
edricew (Director). (2020, November 17). Import and Export in Nomad Sculpt [Video recording]. https://www.youtube.com/watch?v=d6n-BGxA4og
Rigor Mortis Tortoise (Director). (2023, April 1). How to EXPORT MATERIALS from Blender to Unity 2023 (Updated) [Video recording]. https://www.youtube.com/watch?v=yloupOUjMOA

GitHub:
https://github.com/EmilieSommer/ButWorse
When playing the game please select the ratio: 2160x1620
