# More Control & Multiple Actors
1. Control Structures
    1. If/Else Statements
    2. For Loops

### If/Else Statements
Now, notice that your robot leaves your screen forever. Very sad, I know...
Let's make it rotate, so that when it hits the edge of the screen it starts at
the beginning again.

To do so, we can use the concept of if/else statements, boolean statements, and
various operators. An if/else statement can be constructed as follows. Only one
of the options will go through.
```javascript
if( 5 == 5 ){
  print("It is true.");
}else{
  print("It is false.");
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
  print("I am young!");
}else if(myAge < 120){
  print("I'm not sure...");
}else{
  print("I may be the oldest person alive!");
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
