# HW 4: *3D Stylization*

## Sonic's Beach Day

(gif of main camera view)

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

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20002651.png?raw=true)

This shader has multiple light supports and melds a custom texture (inspired by the Sora art). This texture is blended most with the shadows and is more subtle for the midtones. There is also rim lighting (also borrowed from the Sora concept art). 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20003843.png?raw=true)

Watercolor Shader:

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20003928.png?raw=true)

This shader was created using this tutorial (add link). I wanted a more subtle watercolor look without using a texture. This shader works well for the sphere but is too subtle in the main scene. This shader also uses rim lighting!

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20003952.png?raw=true)

Vertex Animation Shader: 

(add picture here) 

I added plants that wave in the wind to add depth to the scene and make it more fun. This was accomplished through vertex animation. I used the following [model](https://sketchfab.com/3d-models/claret-tall-seaweed-6a07131b52b34d8992861d3c3ba82a29) to accomplish this. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20004009.png?raw=true)

Water Shader with Foam: 

(add picture here) 

I referenced the following tutorial in order to help create this. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20004024.png?raw=true)

Water Shader using Voronoi: 

(add picture here) 

I referenced the following tutorial in order to help create this. 

![](https://github.com/user-attachments/assets/b9182f4f-6d78-4ec5-a16f-55e25d2941dd)

---
## 3. Outlines

Post Process Outlines:

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010346.png?raw=true)

I had help from the following [tutorial](https://www.youtube.com/watch?v=VGEz8oKyMpY) to create the outlines. I tried the linked tutorials but ran into technical difficulties. I adjusted the lines to be rather subtle because otherwise (with the dither and the hull shader), it looks rather overwhelming. This shadergraph works via buffer nodes (blit, for making sure lines are separated by color, and normal), and the shader is added as a render feature to the URP. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010205.png?raw=true)

Additional Outlines (to add a fun crayon-like effect): 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010319.png?raw=true)

This was accomplished using the [Hull Shader](). I added distortion to this outline shader using noise that changes based on time. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010150.png?raw=true)

---
## 4. Full Screen Post Process Effect

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010403.png?raw=true)

I used a dither post-process effect to reference the older Sonic games' pixel art style. This looks better in Unity-taking a screenshot added a weird circle texture for some reason. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010135.png?raw=true)

## 6. Interactivity
By pressing the space bar, the shaders get swapped in the scene. 

(add gif)

## 7. 3D Scene (Turn Around)

(add turn around to show it's a 3d scene) 


## Submission
1. Video of a turnaround of your scene
2. A comprehensive readme doc that outlines all of the different components you accomplished throughout the homework. 
3. All your source files, submitted as a PR against this repository.


## Attribution:
Skybox:
[Seaweed 3D Model](https://sketchfab.com/3d-models/claret-tall-seaweed-6a07131b52b34d8992861d3c3ba82a29)
Sonic 3D Model: Unfortunately, I'm not sure where this is from originally, but I borrowed it from the lab assignment.  
Beach 3D Model/Texture: 
