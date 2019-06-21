# Dynamic Images

In this section, we aim to learn about interactivity and how to make your robots
dynamic by using control structures. We also examine various ideas from the code.
1. About
2. Functions
3. Variables
 - Robot Movement
4. Control Structures
 - If/Else
 - For Statements

---

## About

**Variables** store your data in a easier to read and handle format.
**Control structures** help you hand different conditions that come into play.

---
## Functions

Previously, you wrote a lot of code like below:
```javascript
ellipse(... , ... , ... , ...);
square(... , ... , ... , ...);
rect(... , ... , ..., ...);
```

Those functions work by defining a **function definition** like you are doing with
setup and draw. The curly braces tell you when to start and stop defining your
function! That's why it is important to write your code inside the curly braces!

```javascript
function setup(){
  // Definining stuff inside here
}
setup() // When you click the play button, setup is called!
```

Note that functions can have **input variables**. This is how ellipse and the other
shapes you have used work. They take these input variables, do something to them
and allow them to appear on the screen! Here is an example of a function!

```javascript
function add_one(x){
  return x + 1;
}

function setup(){
  // ... Your other code ...
  print(add_one(2)); // This will result in 3 being printed!
}
```

### Task 0
```
Encapsulate your robot into a function, and call your function in draw!
```

---

## Variables

You have seen variables before in `windowWidth` and `windowHeight`. At some
point, they were declared before you had even realized it. That's the benefit (maybe
downside) of using a library! They look like this somewhere in the library code.
```javascript
var windowWidth = 1500;
var windowHeight = 1500;
```
Officially, **Variables*** are named locations for storing a value.

There are two ways to declare a variable. The first way is `var`. The second
way is `let`. The difference is that `var` can last throughout the program while
`let` is block scoped, which means that it works only for a specific block
scope like within a function. Thus, for our purposes, we will suggest using
`var` until you get a handle of scoping.
```javascript
let windowWidth = 1500;
let windowHeight = 1500;
```

At some point, you will realize that encoding coordinates and colors is somewhat
annoying and you will forget that a number like `100` is the color gray in
grayscale. So, we declare variables outside of the functions:

```javascript
// We store the variable gray as 100.
var gray = 100;

// Then, in our function setup, we can have
function setup(){
  // ... Your other code ...
  background(gray);
  // ... Your other code ...
}
```

In another use case, you can write out all of your coordinates relative to say a
starting value like the origin.

```javascript
// Suppose your screen size was windowWidth = 500 and windowHeight = 500
// Instead of having an ellipse at (250, 250), you get the same functionality
// this way:
let halfWindowX = windowWidth / 2;
let halfWindowY = windowHeight / 2;
ellipse(halfWindowX, halfWindowY, 20, 20);
```

### Task 1
```
Create variables to store your hard-coded coordinates and use the variables in
your shapes.
```

---

## Movement

### Moving Your Robot
One easy way to make your robot move is to transform coordinate frames. You can
do this by taking advantage of the fact that draw runs X number of times per second.
```javascript
var position = 0;
function draw(){
   translate(position, 0); // Moves the robot in the X direction.
   position = postion + 1; // You can re-assign variables!
   // print(position) will tell you where the position is.
}
```

### Task 2
```
Make your robot move across the screen!
```

### If/Else Statements
Now, notice that your robot leaves your screen forever. Very sad, I know...
Let's make it rotate, so that when it hits the edge of the screen it starts at
the beginning again.

To do so, we can use the concept of if/else statements, boolean statements, and
various operators. An if/else statement can be constructed as follows. Only one
of the options will go through.
```javascript
if( 5 == 5 ){
  print("It is true.")
}else{
  print("It is false.")
}
```
Javascript uses a boolean type that has two values: `true` and `false`. It's a
way to denote two options. From above, you can compare various operators and
produce the desired equality statement inside your if condition.
```javascript
1 == 1  // true
1 != 1  // false
1 > 1   // false
1 < 1   // false
1 >= 1  // true
1 <= 1  // true
```
Additionally, if statements can be run by themselves or with `else if`, which
allows for more options. Again, only one option will happen.
```javascript
let myAge = 100;
if (myAge < 21){
  print("I am young!")
}else if(myAge < 120){
  print("I'm not sure...")
}else{
  print("I may be the oldest person alive!")
}
```

### Task 3
```
Make your robot circle back to the beginning on the screen.
```

The library allows for a nice mouse click event to happen.
```javascript
if (mouseIsPressed){
  // do something
}else{
  // do something else
}

```
### Task 4
```
On a mouse click, make your robot change colors!
```


### For Statements
For statements allow you to do multiple things. We must follow the exact syntax.
```javascript
// let i=0 creates the variable that won't be used after the for statement
// i < 5 is the stopping condition
// i++ is another way to write i = i + 1
for(let i=0; i < 5; i++){
   print(i);
}
// This will print:
// 0
// 1
// 2
// 3
// 4
```

One thing to notice, however, is that using `translate` modifies the coordinate
system on your screen. So, if you add a new shape, it won't be where you expect!
It will have moved along with the translated frame. So, we will not use this.
Rather, because you have converted all your coordinates to variables, we can
modify the robot position directly.

### Task 5
Make multiple robots.
