<h1>Week-2 Java Deep Dive & Developing Game UI </h1>

Hi there. We are now into week 2.<br>
Last week we covered stuff like installing android studio, gdx libraries and learned some basics of java.<br>
This week, we cover some more aspects of Java and then get our hands on to developing our first Game "Flappy Bird"<br>

Sounds exciting? Let's get started

<h1> Java Deep Dive</h1>
Here we are going to cover classes,objects & methods.
Again referring to <a href="http://iiti.ac.in/people/~tanimad/JavaTheCompleteReference.pdf">this</a> textbook, pages to read are<br>
Pg 105-115 (skip in-depth explanation).<br>
  
Ok then, we are finally now in a position to develop our game. This week,we will clone the flappy bird UI.<br>

<h1> Developing The Game UI</h1>
<br>
Lets start by making a new project. Configure your project to be like <a href="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/libgdx.png">this</a>.<br>
Then dowload flappy bird assets from <a href="">here</a>.Extract the zip, copy all the png files and place it in android>assets folder<br><br>
We are primarily going to work with textures and sprite batches.<a href="https://github.com/libgdx/libgdx/wiki/Textures,-textureregion-and-spritebatch"> Read here.</a><br>
Change the orientaion of the screen by navigating to manifest file and setting screen orientation to portrait.<br>
As we want the bird to be flapping, we are going to use two images of the bird. Create two textures bird1 and bird2 and initialize the variables. Do not forget to also initialize the background variable<br><br>
Moving on to the render method, we are going to draw these images one by one. First draw the background using batch.draw() method. This method can take anywhere from 3 arguments to 5 arguments.For our background image, the first argument will be initialized texture variable, second & third argument - (x,y)coordinate from where the image would start drawing , fourth & fifth argument - width and height of the image to be drawn.<br>
Now to fill the whole screen of the device, we can use <b>Gdx.graphics.getWidth()</b> & <b>Gdx.graphics.getHeight</b> to get the width and height of the device screen. This method would be called many times in our program in the future, so get used to using it.<br>
Similarly we can now draw image for the bird. We can center the bird by getting the height and width of the screen and divide it by 2.<br>
Your final code should look something like this.<br>
<img src="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/code-pt1.png" alt="loading"><br>
