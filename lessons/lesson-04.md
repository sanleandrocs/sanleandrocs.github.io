# Falling Rocks
0. Review Last Week
1. Syntax + Scoping
2. Multiple Actors
   1. Randomness
   2. Score
   3. End Game


## Syntax + Scoping

After coding for a little while now through the previous lessons, we would like
to enforce the idea of scope, what the computer sees relative to the braces that
you type.


#### Function Declaration
```javascript
function greater_than_5(x){
  if (x > 5){
    print(x + " is greater than 5!")
  }else{
    print(x + " is not greater than 5!")
  }
}

function setup(){
  greater_than_5(3);
  greater_than_5(6);
}
```

The function declaration above and below are the same! Note that they are
similar in that a function is declared with the keyword `function
name_of_function (var1, var2, ...) {}`.

```javascript
function greater_than_5(x)
{
  if (x > 5){
    print(x + " is greater than 5!")
  }else{
    print(x + " is not greater than 5!")
  }
}
```

You can write this entirely in one line too! So, the distinction is that having
the elements for the function is more important than the spacing. However, the
spacing allows the code to be easy to read/modify in the future. Keeping a
consistent format is more important than which format you use. Many software
engineers use tools called linters to "prettify" their spacing.

`function greater_than_5(x){if(x>5){print(x+" is greater than 5!")}else{print(x+" is not greater than 5!")}}`

#### Variable Declaration

```javascript
// The two lines of code below are equivalent! Whitespace doesn't matter
// to the interpreter.

// let x =     5;
// let x=5;
```

There is one key idea, however, in understanding scope for our purposes.

The code below does not work because x is defined in the scope of the function.
When a variable is declared inside a function, it only lives until the function
ends. So, in p5js, you will probably get an error like `Uncaught ReferenceError:
x is not defined`.
```javascript
def print_5(){
   let x = 5;
   print(x);
}

print(x);
```

Alternatively, when you declare an element in the code outside of your
functions, you can use them inside of your function!
```javascript
var x = 5;
def print_5(){
   print(x); // This prints 5 and you can use x's scope from outside the function!
}

```

Takeaways
1. Syntax matters in opening and closing braces but whitespace doesn't really matter.
2. Scoping inside and outside the function is different!


## Multiple Actors

#### Task 1
```
Make a rock appear from the sky and fall down to the ground. When they hit the
ground, loop from the top again.
```
### Randomness

Using the [random function](http://p5js.org/reference/#/p5/random), you can get
a random number.

```javascript
let x = random(0, 100); // x is a random number between 0 and 99 (inclusive).
```

#### Task 2
```
Make a rock appear from a random location in the sky.
```

### Score
#### Task 3
```
Display a score somewhere on your screen with the text function.
If the rock touches the ground, increase the score.
```

### End Game
```
End the game if your actor touches the rock.
```
