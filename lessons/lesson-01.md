## Outline

1. Intros (Instructors & Students) - 5 min
2. Describe Program - 10 min
4. What is Computer Science? - 10 min
6. Processing Tasks - 1-1.5 hrs

---

## Preparation

1. Make an account on [https://www.openprocessing.org/](https://www.openprocessing.org/).

---


## Introduction

**Intros**

Herrick, James, Nancy, Vanessa, Taisei

**Describe Program**

Goals:

1. Expose CS earlier to students in San Leandro, who may not have access.
2. Show that CS is exciting and fun to work with.
3. Build some intuition and familiarity with computing concepts.

Ask Questions!
We may forget to introduce some concepts, but asking questions will help you and your peers.

**What is Computer Science?**

- Ask students to write down their definition of CS and discuss in groups!
- Describe.

    > Computer science is the study of processes that interact with data and that can be represented as data in the form of programs. It enables the use of algorithms to manipulate, store, and communicate digital information. A computer scientist studies the theory of computation and the practice of designing software systems. -Wikipedia

    CS ≠ Programming

    > "Programming is the process of designing and building an executable computer program that carries out a given computing task" - Wikipedia

    Programming is a subset of CS.

---

## Processing Lesson and Tasks

A. Opening Screen
   1. Create a 'Create a Sketch'
   1. Click play and circles will appear on your screen wherever your mouse is.
      - Inside the code (</>), you'll find a setup function and a draw function that contains code.
      - Look up documentation by searching in taskbar tab labeled reference. For instance, if you look up `setup()`, you get [here](http://p5js.org/reference/#/p5/setup).
         - Note that there is an **example**, a **description** of the function, and **syntax** (rules to make the computer understand what you want to write. You will spend a lot of time looking at your code and
            looking back at this documentation for each function.

B. Task 1: Make an ellipse appear in the middle of the screen. Use the syntax of the ellipse function to change the coordinates.
   1. To help, modify the function to print the height and width. Type this EXACTLY in your code:
      ```javascript
      function setup() {
        createCanvas(windowWidth, windowHeight);
        print(windowWidth);
        print(windowHeight);
        background(100);
      }

      function draw() {
        ellipse(mouseX, mouseY, 20, 20);
      }
      ```
   2. The screen has a width and height depending on your current monitor. The top left corner starts at (0,0). The bottom right corner is at (windowWidth, windowHeight).

C. Task 2: Take a blank sheet of paper or graph paper and draw a robot.
   1. A robot can be a blender, vacuum cleaner, or anything!

D. Task 3:
   1. Convert your hand-drawn robot into life using processing. Use the steps from Task 1 and documentation from the opening screen.
   
   Tip: to set (0,0) to the center of the display window, insert the command _translate(width/2,height/2);_ into the draw function as follows
   ```javascript
      function setup() {
        createCanvas(windowWidth, windowHeight);
        background(100);
      }

      function draw() {
        translate(width/2,height/2);
        ellipse(mouseX, mouseY, 20, 20);
      }
      ```
   2. The 2D primitives [here](http://p5js.org/reference/) will help you a lot!

E. Task 4:
   1. After making your shapes, add color using the `fill()` function found [here](http://p5js.org/reference/#/p5/fill).
