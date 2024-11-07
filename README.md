# HW 4: *3D Stylization*

## Sonic's Beach Day

![](https://github.com/thumun/hw04-stylization/blob/main/Untitled%20video%20-%20Made%20with%20Clipchamp%20(1).gif?raw=true)

## 1. Picking a Piece of Concept Art

I was initially inspired by this concept art from Kingdom Hearts of Sora (and from there, I wanted to do a watercolor beach scene): 
![Kingdom Hearts Concept](https://github.com/thumun/hw04-stylization/blob/main/b965c604nadb1%20(1).png?raw=true)
I unfortunately cannot find the original artist for this piece, but I believe it may be official art/concept art, so in that case, the art is most likely from the official Kingdom Hearts art team.

However, I could not find any (not creepy) models of Sora and, unfortunately, did not have the time to make one myself. So, I borrowed the sonic model from lab! To pay homage to the sonic model, I put a twist on the concept art to look more video game-y (on top of the watercolor shaders). Here are some examples of what I had in mind (all from Sonic Mania): 

| ![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20013751.png?raw=true) | ![](https://github.com/thumun/hw04-stylization/blob/main/sonic-team-pixel-art-is-not-viable-games-with-pixel-art-v0-j1tdvxvyojlb1.png?raw=true) | 
|:--:|:--:|
| *Sonic Mania* | *Sonic Mania* | 

---
## 2. Interesting Shaders

Toon Shader with a custom texture (for the shadows and midtones): 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20002651.png?raw=true)
![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20012126.png?raw=true)

This shader has multiple light supports and melds a custom texture (inspired by the Sora art). This texture is blended most with the shadows and is more subtle for the midtones. There is also rim lighting (also borrowed from the Sora concept art). 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20003843.png?raw=true)

Watercolor Shader:

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20003928.png?raw=true)
![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20012116.png?raw=true)

This shader was created using this [tutorial](https://cyangamedev.wordpress.com/2020/10/06/watercolour-shader-experiments/). I wanted a more subtle watercolor look without using a texture. This shader works well for the sphere but is too subtle in the main scene. This shader also uses rim lighting!

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20003952.png?raw=true)

Vertex Animation Shader: 

![](https://github.com/thumun/hw04-stylization/blob/main/Untitled%20video%20-%20Made%20with%20Clipchamp%20(2).gif?raw=true)

I added plants that wave in the wind to add depth to the scene and make it more fun. This was accomplished through vertex animation. I used the following [model](https://sketchfab.com/3d-models/claret-tall-seaweed-6a07131b52b34d8992861d3c3ba82a29) to accomplish this. A clip with the plants can be seen in the gif at the top of the readme. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20004009.png?raw=true)

Water Shader with Foam: 

The foam is animated and there is a slight opacity to the water. This can be seen in the image above!

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20004024.png?raw=true)

Water Shader using Voronoi: 

I wanted an additional water shader for the material swap that has more of a 'toon shaded' look to it (similar to Wind Waker). The water is animated using voronoi noise. This can be seen in the image above!

![](https://github.com/user-attachments/assets/b9182f4f-6d78-4ec5-a16f-55e25d2941dd)

---
## 3. Outlines

Post Process Outlines:

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010346.png?raw=true)

I had help from the following [tutorial](https://www.youtube.com/watch?v=VGEz8oKyMpY) to create the outlines. I tried the linked tutorials but ran into technical difficulties. I adjusted the lines to be rather subtle because otherwise (with the dither and the hull shader), it looks rather overwhelming. I also only wanted Sonic to have outlines. This shadergraph works via buffer nodes (blit, for making sure lines are separated by color, and normal), and the shader is added as a render feature to the URP. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010205.png?raw=true)

Additional Outlines (to add a fun crayon-like effect): 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010319.png?raw=true)

This was accomplished using the [Hull Shader](). I added distortion to this outline shader using noise that changes based on time. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010150.png?raw=true)

---
## 4. Full Screen Post Process Effect

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010403.png?raw=true)

I used a dither post-process effect to reference Sonic Mania's pixel art style. This looks better in Unity-taking a screenshot added a weird circle texture for some reason. 

![](https://github.com/thumun/hw04-stylization/blob/main/Screenshot%202024-11-07%20010135.png?raw=true)

## 6. Interactivity
By pressing the space bar, the shaders get swapped in the scene. This can be seen in the first gif at the top of the readme. 

## 7. 3D Scene (Turn Around)

![](https://github.com/thumun/hw04-stylization/blob/main/Untitled%20video%20-%20Made%20with%20Clipchamp%20(3).gif?raw=true)


## Attribution:
[Tropical Island Skybox](https://sketchfab.com/3d-models/free-skybox-tropical-island-ccc22ba1a2af4e40b467ce1e21215caa)

[Seaweed 3D Model](https://sketchfab.com/3d-models/claret-tall-seaweed-6a07131b52b34d8992861d3c3ba82a29)

Sonic 3D Model: Unfortunately, I'm not sure where this is from originally, but I borrowed it from the lab assignment.  

[Beach 3D Model/Texture](https://assetstore.unity.com/packages/3d/props/exterior/super-beach-pack-39084?srsltid=AfmBOooikKJLsuwQMQo53itSFpdKhTL31wnc5IXIzvgpeLd8_HxAfghu)
