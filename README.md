# HW 4: *3D Stylization*

## 1. Picking a Piece of Concept Art

I was initially inspired by this concept art from Kingdom Hearts of Sora (and from there, I wanted to do a watercolor beach scene): 
![Kingdom Hearts Concept]([https://github.com/CIS-566-Fall-2023/hw04-stylization/assets/72320867/dae1ffc2-8269-493d-919f-b3811c76ed30](https://i.redd.it/b965c604nadb1.png))
I unfortunately cannot find the original artist for this piece, but I believe it may be official art/concept art, so in that case, the art is most likely from the official Kingdom Hearts art team.

However, I could not find any (not creepy) models of Sora and, unfortunately, did not have the time to make one myself. So, I borrowed the sonic model from lab! To pay homage to the sonic model, I put a twist on the concept art to look more retro video game-y (on top of the watercolor shaders). Here are some examples of what I had in mind: 

| ![](https://github.com/CIS-566-Fall-2023/hw04-stylization/assets/72320867/dae1ffc2-8269-493d-919f-b3811c76ed30) | ![](https://github.com/CIS-566-Fall-2023/hw04-stylization/assets/72320867/9c345ee6-19df-4191-9e47-6722b6597a5a) | ![](https://github.com/CIS-566-Fall-2023/hw04-stylization/assets/72320867/48521733-f83a-4704-ac8d-9d2f24574922) | ![](https://github.com/CIS-566-Fall-2023/hw04-stylization/assets/72320867/3068bdc4-1b08-41cf-9a16-08d94be5f1ea) |  ![](https://github.com/CIS-566-Fall-2023/hw04-stylization/assets/72320867/ae1d0fae-7998-4287-8269-13e2cafd740b) | 
|:--:|:--:|:--:|:--:|:--:|
| *https://twitter.com/stefscribbles/status/1646235145110683650* | *https://twitter.com/trudicastle/status/1122648793009098752* | *https://twitter.com/caomor/status/1049494055518908416* | *https://www.artstation.com/requinoesis* | *https://twitter.com/cysketch/status/1712442821389713597* | 

---
## 2. Interesting Shaders

Toon Shader with a custom texture (for the shadows and midtones): 

(add picture here)

This shader has multiple light supports and melds a custom texture (inspired by the Sora art). This texture is blended most with the shadows and is more subtle for the midtones. There is also rim lighting (also borrowed from the Sora concept art). 

Watercolor Shader:

(add picture here) 

This shader was created using this tutorial (add link). I wanted a more subtle watercolor look without using a texture. This shader works well for the sphere but is a bit too subtle in the main scene. This shader also uses rim lighting!

Vertex Animation Shader: 

(add picture here) 

To add depth to the scene and make it more fun, I added plants that wave in the wind. This was accomplished through vertex animation. I used the following [tutorial](https://www.youtube.com/watch?v=VQxubpLxEqU&ab_channel=GabrielAguiarProd) and the following [model](https://sketchfab.com/3d-models/claret-tall-seaweed-6a07131b52b34d8992861d3c3ba82a29) to accomplish this. 

Water Shader with Foam: 

(add picture here) 

I referenced the following tutorial in order to help create this. 

Water Shader using Voronoi: 

(add picture here) 

I referenced the following tutorial in order to help create this. 

---
## 3. Outlines

Post Process Outlines:


I had help from the following [tutorial](https://www.youtube.com/watch?v=VGEz8oKyMpY) to create the outlines. I tried the linked tutorials but ran into technical difficulties. 

Additional Outlines (to add a fun crayon like effect): 


This was accomplished using the [Hull Shader](). 

---
## 4. Full Screen Post Process Effect

(add picture)

I used a dither post-process effect to reference the older Sonic games' pixel art style. 

## 6. Interactivity
By pressing the space bar, the shaders get swapped in the scene. 



## Submission
1. Video of a turnaround of your scene
2. A comprehensive readme doc that outlines all of the different components you accomplished throughout the homework. 
3. All your source files, submitted as a PR against this repository.


## Attribution:
Skybox:
[Seaweed 3D Model](https://sketchfab.com/3d-models/claret-tall-seaweed-6a07131b52b34d8992861d3c3ba82a29)
Sonic 3D Model: Unfortunately, I'm not sure where this is from originally, but I borrowed it from the lab assignment.  
Beach 3D Model/Texture: 
