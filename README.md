(in progress)
Weclome to my esoteric language [cool name]!

From Wikipedia:
"An esoteric programming language (sometimes shortened to esolang) is a programming language designed to test the boundaries of computer programming language design, as a proof of concept, as software art, as a hacking interface to another language (particularly functional programming or procedural programming languages), or as a joke."

This will not be a language designed to test the boundaries of computer programming.

Here's the vision for the language:
  - Create and write the program in the special language we're going to make
  - After writing your code, request a prompt from the compiler/interpreter (need to figure this out).
  - Organize and shape the code so that it looks like a picture of the given prompt (which could be duck or windmill or whatever)
  - If your picture is good enough, the code will run. If not, upon failure you will be given a new prompt to try again.


So there's a whole bunch of things we need to do:
  - Create our own programming language
    - There is zero chance I'm writing a compiler for the language, as that needs extensive knowledge of low-level programming and assembly.
    - Instead I'm just gonna create an interpreter with Java 🙂.
    - We need to also figure out what features we want and what the syntax will be.
    - We will then need to create a context-free grammar to parse our code and handle it.
    - That should be good enough for now.
  - Create a neural network to identify whether the code looks like a picture of the given prompt.
    - For this I'm gonna use the open source quick-draw dataset (https://github.com/googlecreativelab/quickdraw-dataset/tree/master), which has a lot of training data.
    - Obviously I won't be using the whole dataset as it's massive... I'll pick a size as I see fit.
    - Then I'll need to build my own neural network from scratch, which isn't too difficult (I think).
    - I'll probably use 80% of my dataset to train the model and then use the remaining 20% to score the model and see its performance.
    - Ideally I want my neural net to be >90% accurate, but again, all these numbers are subject to change.
  - Create a program handler that will give the prompts and handle program execution (or rejection).
    - This will hopefully be the easiest step, I'll set up a terminal command that initiates the following process:
      - It is initially invoked through something like 'please run <program>' (you have to be kind).
      - It will return a prompt and wait, upon which you need to modify your program to create the picture.
      - You then signal that you have modified the program, typing something like "done".
      - If it doesn't like the drawing, it'll signal failure and give a new prompt. If it likes the drawing, it will say that it is happy with the code and will run it. 
      - You must then thank the handler for its hard work, saying something like "Thank you for running this program for me".
      - If you fail to show gratitude, it will get angry and refuse to compile the code, requiring a restart.
    - I'll try to hide/protect the correct program interpreter if I feel like it so you can't easily compile it using that. You will have to use the artsy program handler.
   
