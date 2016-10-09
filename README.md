#BlockE

You can find our project at: https://drive.google.com/file/d/0B3BmeIJleAeeTnpJN000UEJDT1k/view?usp=sharing

## Inspiration

Limits have been shattered with advancements in augmented reality. These limits have been shattered in every industry, especially entertainment and education. Block-E aims to change the way we play and learn through blocks. 

Problems with current block games like LEGO:
- Easy to lose blocks
- Blocks are very expensive, especially custom blocks for sets
- Blocks are limited, they can only be used once in a creation
- Can be hard to pry apart blocks
- Stepping on them hurts!!!
Block-E eliminates all of those problems through visualizing everything. Since all blocks are digitized, they're impossible to lose, they're easy to replicate and the user has access to an infinite amount of blocks. Blocks can be used in any creation, and multiple creations can be saved by one user with ease. The interface is incredibly easy to work with - users can change entire swaths of blocks' color through a couple of clicks, and can separate pieces through deleting them with a single airtap. Best of all - stepping on a holographic block does no damage, unlike regular LEGOs.

Block-E can change the way we approach education. By using a modular codebase, Block-E can change the way we teach robotics and inspire creativity in the household. Virtual simulations let students create and explore to their hearts content. The limitation is no longer infrastructure, but rather, their creativity.

## What it does

Block-E is a virtual platform for block development. Built on a highly flexible framework, Block-E combines the best of the virtual and real world to make an augmented reality app that transcends real life. Through blocks, the application revolutionizes block building games. By virtualizing everything, Block-E offers more flexibility and features than current systems, at a much cheaper cost. Block-E lets the user select from an array of bricks and colors to sculpt large creations in a virtual environment. 

## How we built it

The HoloLens application was entirely built in Unity3D. We first created the application for PC. Using a free movement camera, we tested the application until we finished all the basic functionality. Because deploying to Hololens was heavily delayed due to IP connection issues, most of the code was initially created for PC gameplay. Once we got Hololens working, we moved onto pure Hololens development. Despite all the setbacks, we were able to port the entire framework into Hololens. 

## Challenges we ran into

The number one challenge was the use of HoloLens from an application originally designed for PC. We had originally created the application for use in the Unity Editor, including having commands like OnMouseEnter. When we had to shift it to HoloLens, everything was simple in the manner of changing the commands to something like OnGazeEnter. However, for the first 17 hours of the hackathon, we were unable to deploy to HoloLens. 

### Deployment Issues
Though one of our computers was able to interface to the HoloLens, the main Unity coder was unable to connect to the HoloLens. Multiple mentors from Microsoft and Unity were perplexed as to the source of the issue - Visual Studio was updated, the device was repaired, the computer and device restarted several times, but to no avail. Everytime the project built and got ready to deploy, Visual Studio would complain and crash. 
The problem was that the IP service on the laptop - one of the mentors ran a command in command prompt which enabled the computer to interface to the HoloLens - but by then it was midnight and 17 hours were gone. 

### Saving
Our second major issue was saving. Unlike the simple saving techniques of a computer, Universal Windows Platform is significantly more complex and requires different storage protocols. The challenge took the majority of the second day, but was a very important problem that needed to be solved in order to finish the product. 


## Accomplishments that we're proud of

### Shared Worldview
Playing with blocks as a child was mostly a multiplayer experience. As a kid, we visited other friends' houses in order to create together. This point is not lost upon us. Using Hololens's world coordinate sharing system, we let users share their experience with other Hololens users. This adds another dimension in Block-E. 
We accomplished this through use of a laptop to create a service. We will create a client app in the future to streamline this process. The two Hololens's connect to the same service and through spacial mapping, can sync their worlds. 

### Saving
One of our largest problems was finding a proper way to save user creations to be reopened at a later time. Being able to save is an essential part of any creation application. Initially we planned on using XML serialization to save on the Hololens drive similar to saving on a PC, but things weren't so simple. Saving and reading from files on Hololens is in its very early stages, and right away, we know that things were going to get messy. Our goal was to serialize an array of objects, obtain a string, and write it to a json file. Unfortunately, the libraries capable of saving files regularly on a computer were incompatible with the ones under the Universal Windows Platform (UWP) needed to save files on a Hololens device. Furthermore, there is no possibility to open a dialog for saving a file in a certain location. Despite the fact that a temporary location and file name needed to be hard-coded into the code for exporting, we managed to run the app, and to add a voice command for this functionality. 

### Flexible Codebase
We're very proud of our highly flexible codebase. The block system is very modular, meaning a database of hundreds of types of blocks can be easily integrated into the game. The flexible system also lets the user incorporate different block types. Though we only have 3 prototype blocks to showcase the application, the user can theoretically link plates, tiles,hinges and other complex blocks. 

## What we learned

The entire experience was an excellent way to get familiar with Microsoft HoloLens and AR devices. We learned the differences between developing on Universal Windows Platform compared to regular applications. Specifically, we learned the most through the problems we solved. 

- System storage architecture - the best way to serialize and save files on UWP and regular PC's. 
- Augmented Reality development - the differences between augmented reality and virtual reality, and the applications
- Design principles - there are ways to create HUD UI and create user-friendly experiences that are intuitive and comfortable - one of the most important things we learned at this hackathon
- Professional design - our team is entirely made of students (two of us are high schoolers). At this hackathon, we were able to watch and learn from professional 
