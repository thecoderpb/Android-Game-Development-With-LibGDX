<h1>Week -4 Scoring,GameOver Screen & Optimization</h1>
Welcome to the last week of this course. By now you have the basic knowledge on how to build a game.<br>
This week will be quite general. It's on how to improve efficiency of your code and speeding up development. Before that, if you had
issues working with score logic and developing gameOver screen, lets get over that quickly.

<h1> Scoring and GameOver Screen</h1>
The idea is to check it the tube has passed from the screen, if so then increment the score by 1.<br>
An additional conditional check of the tube to be less than number of tubes ie 4 is necessary.
<img src="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/scoring.png" alt="loading"><br?
Now the score is incrementing but we really can't see it. To display it, we are going to use a class called BitmapFont.<br>
<img src="https://raw.githubusercontent.com/thecoderpb/Android-Game-Development-With-LibGDX/master/blobs/font.png" alt="loading"> <br>
<br>
Coming to the last part of setting up game over screen, it's pretty easy. Just change game state to 2 and check in outer most if statement if it is
true. If true, we can capture the state of the game and display a game over message. Easy right?<br>
The full code can be found <a href="">here</a>

