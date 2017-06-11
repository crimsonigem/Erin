 # Harvard iGEM 2017 Week 1 (6/5 - 6/9)


## Software, Website, and Wiki Development

This week I focused on getting familiar with various development tools such as javascript and python packages.

### [Processing.js](http://processingjs.org/)
Used for data visualization, digital art, and interactive animations.

Basic usage tutorial:
1. Download processing.js file in the same directory folder
2. Create <filename>.pde in the same directory folder
3. Insert into html just like any other files

Basic explanation of the code:
1. void setup ( ) {creates initial canvas}
2. void draw ( ) {actual drawing function: "erases" and "redraws" by frame to give the effect by animation. To make the art interactive, include mouse tracking component.}

### [D3.js](https://d3js.org/)
Used for interactive data visualization

Basic usage tutorial
1. Download d3.js file in the same directory folder or refer to the newest version by url

Basic explanation of the code:
1. Each chunk of the data is considered as a node and each node can be edited separately
2. Allows for flexible editing of the data points, as well inclusion of additional nodes

### [Physics.js](http://wellcaffeinated.net/PhysicsJS/)
Used for simulating the physics of interacting objects (gravitational fall, diffusion)

Basic usage tutorial
1. Download physics.js in the same directory folder
2. Envelope physics.js code in the physics function (explained below)

Basic explanation of the code:
1. All physics.js code begins in the creation of the physics world:
  * Physics(function( world ){// code here...});
2. Create canvas
3. Add renderer with appropriate function, calling the canvas created previously with the appropriate ID
4. The physical properties of the objects are handled by the physics.<function> so the "erasing" and "redrawing" does not explicitly need to be coded

### [Pymol](https://www.pymol.org/)
Visualization of 3D protein models

Basic usage tutorial
1. Download pymol desktop program

![alt text](https://pymolwiki.org/images/2/20/Viewer_guide.png)

  * The left part of the window is the visualization of the protein file
  * **Object Control Panel:** tools for showing viewing options, toggle visibility, etc
  * **Mouse Control Legend:** Cheat sheet for mouse controls
  * **Selection Tools:** Tools for selecting specific parts

*Basic guide courtesy of <https://pymolwiki.org/index.php/Practical_Pymol_for_Beginners>. Visit the website for more specific instructions*

### [PySBOL](https://github.com/SynBioDex/pySBOL)
Module for reading, writing, and constructing genetic designs according to Synthetic Biology Open Language (SBOL). Similar to LaTeX in standardized notation of genetic constructs.

Basic usage tutorial:
1. Download package and place in same folder directory
