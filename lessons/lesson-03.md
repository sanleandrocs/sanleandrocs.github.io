# More Control & Multiple Actors (Part 2)
1. Control Structures 
    1. If/Else Statements
    2. For Loops
2. Multiple Actors

## Control Structures

### If/Else Statements
Notice that your robot leaves your screen forever. Very sad, I know...
Let's make it rotate, so that when it hits the edge of the screen it appears at
the other side of the screen again.

To do so, we use if/else statements. An if/else statement can be constructed as follows. 
**Only one of the blocks will go through.**
```javascript
if( 5 == 5 ){
  print("It is true.");  // Either this happens
}else{
  print("It is false."); // or this, but not both
}
```
Javascript uses a boolean type that has two values: `true` and `false`. It's a
way to denote two different options. From above, you can compare various operators and
produce the desired equality statement inside your if condition. Some examples of operators
include: 
```javascript
1 == 1  // true 
1 != 1  // false
1 > 1   // false
1 < 1   // false
1 >= 1  // true
1 <= 1  // true
```
If statements can also use `else if` to add extra options.
Again, only one block will happen.
```javascript
let myAge = 100;
if (myAge < 21){
  // Either this runs
  print("I am young!");          
}else if(myAge < 120){
  // Or this
  print("I'm not sure...");
}else{
  // Or finally, this
  print("I may be the oldest person alive!");
}
```

### Task 3
```
Make your robot circle back to the beginning on the screen.
```

The library we use, p5js, allows for an easy way to handle mouse click events.
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

## Multiple Actors
Now, you have the basics of how programs works. The next step is to build more
familiarity. So, make more robots!

### Task 6
```
After modifying your original robot. Make another robot appear on the screen that
interacts with your original robot.
```
