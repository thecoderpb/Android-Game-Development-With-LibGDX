<h1>Week -3 Collision Detection </h1>
Welcome to week 3. Half way done, half way to go.<br>
If last week was quite overwhelming to you, this week will not be :p<br>
<br>

Now since our UI is up and running, it is not interacting with each other.
So let's enable collision detected to our bird.

<h1> The ShapeRenderer Class</h1><br>
Basically it draws a detectable shapes on a texture. It renders points, lines, shape outlines and filled shapes.<br>
More info <a href="https://libgdx.badlogicgames.com/ci/nightlies/docs/api/com/badlogic/gdx/graphics/glutils/ShapeRenderer.html">here</a>
Note that this class has nothing to do to our game. Infact we will delete all the code related to this class once we complete our development.
Let's start.
<br><br>

Similar to SpriteBatches, even Shaperenderer class hass begin() and end() methods. We first declare and initialize a Shaperenderer in our program.
Now, we use a math class of GDX under package <b>com.badlogic.gdx.math </b> to draw a circle for the bird and rectangle for the tubes.<br>
Create & initialize the birdCircle variable in the create method. At the end of our render method we use the birdCircle.set() method to make
a circle. The parameters taken by this method are x,y coordinated & radius. Luckily we are good at finding coordinates of any texture, so
go ahead and give it a shot. For the radius, we can take either the width or height of bird and divide it by 2 to roughly cover the entire region
of bird. As usual give it a try, else find the code <a href="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/birdCircle.png">here.</a>
<br>
Now, our circle is drawn onto the bird but we are unable to see it. This is where our shaperenderer comes in handy.Check this code below.
At this point, I hope you would understand the code by yourself.<br>
<img src="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/shapeRend.png"><br>
The shaperenderer circle takes in 3 parameters similar to birdCircle.set() method & since it is defined above by us, we can directly use
its x,y,radius values or copy paste the parameter's to shaperender method. whichever suits best.<br>
Run the code. We see a filled circle drawn onto the bird.<br>
Once done, our next target here would be to do the same to all the rectangles top tube and bottom tube. Again try and give a shot to it,
or find the code <a href="">here.</a><br>
A brief explanation is given below.<br>
<img src="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/shape.png" alt="loading"><br>

Two arrays have been declared. We utilize the existing for loop to initialize our rectangle variables. In the render method we just copy
the values specified in batch.draw() method which gives us x and y coordinates. The height and width are in itself justifiable.
Run the code and see the output.

<img src="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/flappy.png" alt="loading">

So with this, we complete 90% of our coding part. Our game is almost ready.

<h1>Let the collision begin!!</h1>

<img src="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/intersector.png" alt="loading">
<br>
That's it. It's just one line of code.
<br>The intersector.overlaps() as it's name suggest checks if the bird collides with topRectangle or bottomRectangle and if it's true
we change the gameState.
