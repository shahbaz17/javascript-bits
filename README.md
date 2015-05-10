Hey Folks!

This is my `personal` guide of writing Javascript, people are welcome to correct/suggest things or pick the best one out of it.
In course of time I will keep updating it, adding new ones or updating the older ones, so keep a track! :sunglasses:

If you want to suggest a change or have a discussion or wants something to be added, open an issue and we will have a nice brainstorming session.

If you :heart_eyes: it, you can always star this repo and keep a track for more future fun! :wink:

> P.S: I am open for change, if I am wrong somewhere I would be happy if you can help me understand the other way round.

#Writing Style

##Tab or Space
Go with the TAB! Why? I hope you don't want to press the right key that much to go from one end to another of a row so that in its lifetime it looses its color. `#JustKidding`

Its Ok if you have a config setuped VIM for it, but you are wasting Compiler's time by adding those many spaces on every line.

```javascript
  var TAB = '\t'
  var SPACE = ' ' // see, its a space!
```
### Space = 2 | | 4
It depends, I prefer both, those who work on VIM shells gets annoyed with 4 spaces but its Ok, you know.
4 Space helps you easily figure out the blocks, start and end markers because your code is quite openly visualized.

If your code blocks constitutes of small chunks then 2 space will do good but if you are writing heavy lines of code then 2 space might mess up readability.

###Arguments against 4 Space
- *When I see online on git, it sometimes doesn't looks good :disappointed:*

Dude! Git is meant to be forked/cloned and work offline, but yeah if some stalker need a reference from your code then this might be the case in which its OK, they can just scroll.
- *I have to switch between 2 and 4(sometimes even space and tab), I hate that, lets generalise everywhere.*

Its all editor variable that will show things in the way you want to visualize, keep project configs. :smirk:
> **Stay Calm and Use Editor Config**

## Variables
Aah! The very first question that goes on everyone's mind.
```javascript
var var1 = "some-value"
var var2 = "some-another-value"
var biggerVarMessUpEverythingThatYouWroteAbove = "But you can ignore it! :)"
```
Things that you would have noticed:
- A single space surrounding ```=``` is a good practice
- Indentation: This is a tricky part, sometimes I do, sometimes I don't. Check the next section.
- Semicolons? Seriously? I don't have much time in adding semicolons when I am just declaraing variables, gives a clean look to my code.
- Variable names should be small, concise and precise, `itMakesNoSenseInHavingALargeVariableName`

### Bad Ways
```javascript
var these, make, sense;
var var1, var2="ThisOneSucks", var3="ThisOneToo";
var v                                                 = "IAmSmallButIHaveAVeryLargeValue"
var IHaveBigNameSoIMakePeopleStretchTheirComfortZones = "Meh"
IDontCareAddingVarInMyName                            = "LikeABoss"
```
- Avoid doing one line instantiation
- Its good to align things, but not always!
- Without a `var`, are you serious? Ok add ```use strict``` at the top of the file

##Indentation
There is a friction in JS developers when it comes to indentation, some have an opinion on never indent things, some wants to indent everything. So here is what I use.

- Always align the declarations/instantiation
```javascript
var var1    = "someValue"
var parser  = require("parser")
// Past declaration, its a new world. So don't try aligning that
// rather add 2 new lines to separate both of them
var someFunction = function(){}
```
- Assignment of values(not instantiation!) doesn't need to be always aligned. If you have a small block of code you can, else refrain yourself from it.
```javascript
function myAwesomeFunction(){
    var i, will, _use, these, variables, later // always keep these kids at the top
    var someVal     = createClass("classA")
    var anotherVal  = createClass("classB")
    
    if (someVal.methodA()){
        i = 1 // if you indent this, it will not be in a readable format
        variables = [1, 2, 3]
        these     = i ? 2 : 3 // indent = optional
    }
}
```
- Any variable `below` a long variable name, deserves to be indented. Your code will look much readable, the down ladder is more human readable then the upper ones.

##Spacing
```javascript
var a = "SomeValue" // surrond the = with space
if (someCondition){ // immediate block start keyword should be a space
  // do something
} else {          // always surround the next consecutive block keyword with spaces
  //do something else
}

var ternary = if ? doThis : else  // surrond these operators with space

function A (arguments){ // a space after the function name
  try { // non param keywords having space is optional
    // try me!
  } catch (e){  // surround catch with spaces
    // if I fail, catch me here!
  }
}
// even I have a space!
```
- Immediate block start keyword with params `(if, switch, function)` should have a space
- Immediate block end keyword `(else, catch)` should have a space
- Ternary Operators `(?, :)` should be surrounded by a space

##New Lines
```javascript
/*

  I am file start comment section
  @authour : Something
  @description : This file's description
  I deserve 2 new lines at the start and end of my block!
  
*/
var someVariable = "someValue"
var anotherVariable = "anotherValue"
var blah            = "Blah" // add 2 newlines between module vars and module body


function XYZ(){
  var inner_var = "xyz"
  var inner_var_two = 2 // single new line between local body and local var declaration
  
  if (someCondition){
    
    /*
      I am a multiline comment body, don't just start writing things just above
      and just below me.
    */
    
    inner_var = inner_var.replace(/(\w+)/gi, "")
    // however you can with me
    inner_var_two = 2>>0X0A
  }
}
// end of the file, new line? Optional.
```
##Comments
```javascript
// I am a single line commnet followed by my brother
// So I can have my first letter capital
var some_variable = "Dude!" // my first letter should'nt be capital
var fcuk_rules    = "Yeah!" // If I have first word as keyword, I can!(optional):wink:

/*
  I am a multiline King Size Panda!
  You can have every line of mine starting with capital letters
*/

function abcClass (arguments){
  //body..
}
```
##Naming Conventions
```javascript
I_AM_GLOBAL = "Global Constant"
Global      = {}  // global Objects should be one word and captilized()

var someModule = require("/modules/some_module") // local required module/class

function someFunction(){  // either camel case variables or functions, not both!
  var some_variable = "some value"
  var someClassInstance = new someModule()
  
  someClassInstance.someMethod(function(_some_variable){
      // If you want to reuse the name in inner block, add an underscore
      if (_some_variable == some_variable){
        return this.someAnotherFunction()
      } else {
        return this.elseWalaFunction()
      }
  })
}

```
#Perfs
> On the way! :rocket: They are under the Optimization booth of mine! Hopefull till this weekend.

> Meanwhile you can have a look at this cute lazy Panda! :stuck_out_tongue:

![Cute Lazy Panda](http://i.kinja-img.com/gawker-media/image/upload/s--ft1APKVa--/18a5kzrhxhqwvjpg.jpg)
