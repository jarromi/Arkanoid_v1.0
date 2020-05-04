# Arkanoid v1.0
### 04.05.2020
### Jaromir Panas

This repository contains files for a task I was given in a recruitment process: create breakout game in C++.
The task also included additional conditions:
1. The game should have 3D graphics and cannot use flat sprites. I have chosen to work with OpenGL, as I found a nice tutorial for this API specification.
2. The game should allow mutliplayer mode: real-time gameplay for two or more players on the same map.

I have chosen to implement an Arkanoid game, with co-op for two players. Here I include files for the first working prototype. It still needs quite a lot of modifications, but the important part is that it works.

#### Dependencies:

I have been working with quite a few APIs that simplify working with OpenGL. Therefore, in order to run the game one needs to get the following:
1. GLWF3 - an API for context creation in OpenGL: https://www.glfw.org/
2. GLAD - Multi-Language GL/GLES/EGL/GLX/WGL Loader-Generator based on the official specs: https://glad.dav1d.de/
3. GLM - math library for OpenGL: https://glm.g-truc.net/0.9.9/index.html
4. stb (actually just stbi_image.h header file) - image loading/decoding from file/memory: JPG, PNG, TGA, BMP, PSD, GIF, HDR, PIC. Source: https://github.com/nothings/stb/blob/master/README.md
5. winsock2 - a library for Windows for creating, connecting and communicating servers, clients, etc.

#### Things to change:

1. Correct the implementation of classes, functionalities, etc. I just wanted to get the working version as quickly as posible, learning everything from scratch. So some classes initially written in one way, were modified in not a very elegant way.
2. Correct the implementation of server - client communication. Right now the communication happens after every frame. If the communication freezes the game freezes as well. What's more the ball propagation is not handled nicely in such an event. It would be best to split gameplay and communication between two processes the exchange data when needed.
3. Enhance gameplay: add more levels, add bonuses (platform widening, shortening, etc.)
4. Make better graphics - now it's quite raw and simple.
5. Make installer: because I have used quite a few APIs, in future it would be nice to create an installer that unpacks/installs them for the user.
