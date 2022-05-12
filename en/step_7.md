## Playing back the moves

Now it's time to playback all the dance moves.

--- task ---
You can begin the playback of the dance when the `space` key is pressed, and hide the list so it does not block the view of the stage.

```blocks3
when [space v] key pressed
hide list [moves v]
```
--- /task ---

--- task ---
To playback each of the moves, you need to keep track of which move you are playing in the `moves`{:class="block3variables"} list. To do this you can create a variable called `position`{:class="block3variables"}. This will start at `1`{:class="block3variables"} and then increase after each move is played.

```blocks3
when [space v] key pressed
hide list [moves v]
+ set [position v] to (1)
```
--- /task ---

--- task ---
Now you need to **iterate** over the `moves`{:class="block3variables"} list. This means looking up the item in the `moves`{:class="block3varaibles"} that is at `position`{:class="block3variables"} and then increasing the `position`{:class="block3variables"} variable by one each time. This will need a loop that will repeat for each item in the list.

```blocks3
when [space v] key pressed
hide list [moves v]
set [position v] to (1)
+ repeat (length of [moves v])
```
--- /task ---

--- task ---
The next stage is to have the sprite perform the dance move in the list, play the drum beat and change the `position`{:class="block3variables"} variable by one.
See if you can try this on your own, and use the hints below if you need help.

--- hints --- --- hint ---
Start by `switching costume`{:class="block3looks"} to the `position`{:class="block3variables"} of the `moves`{:class="block3variables"} list.
--- /hint --- --- hint ---
Here are the blocks you will need:

```blocks
play drum () for (0.5) beats
item () of [moves v]
change [position v] by (1)
(position)
(position)
switch costume to ()
```
--- /hint --- --- hint ---
Here is the completed script within the loop:

```blocks3
when [space v] key pressed
hide list [moves v]
set [position v] to (1)
repeat (length of [moves v])
+ switch costume to (item (position) of [moves v])
+ play drum (position) for (0.5) beats
+ change [position v] by (1)
--- /hint --- --- /hints ---
--- /task ---

--- task ---
Start your program and record a few moves, then press the spacebar to set your sprite dancing.
--- /task ---
