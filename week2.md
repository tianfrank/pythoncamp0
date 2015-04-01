# 3月30日折腾日记
## 大妈谈话和coursera学习
- 1. 大妈谈话
- 2. event-driven program
- 3. local vs. global  
start --- initiate ----wait  
Concepts: *conditional*; *handler*;*function*;*argument*  
Events:  
**Input**  
Button --- handler  
Text box  
**Keyborad**  
Key down  
Key up  
**Mouse**  
Click  
Drag  
**Timer**  
timer = simplegui.create_timer(1000, tick) 2 arguments  
Event Queue  
Event handler  
2. local vs. global variables  
always use local variable  
敲了这两个的Example, 感觉实在地学到了点东西

# 3月31日折腾日记
## simple GUI + Buttons  
### simple GUI  
a frame is the whole user interface frame  
**Program Structure**  
Globals (State)  
Helper functions  
Classes (later)  
Define event handlers  
Create a frame  
Register event handlers  
Start frame & timers  

**BUTTONS**  

print "" 空一行  
frame.add_button("Print", output, 100)  100 is the width  
frame.add_button(text, button_handler, width)
  

# 4月1日折腾日记  
## Input fields + Guess the number version1  
### GTN 1. code  
####  

import simplegui  
import random  
import math  

secret_number = 0  

def new_game():  
    global secret_number    
    secret_number = random.randint(0, 100)      
    pass    
def input_guess(inp):    
    input = int(inp)    
    if input > secret_number:  
        print "Lower"  
    if input < secret_number:  
        print "Higher"  
    if input == secret_number:  
        print "Correct"  
    print "Guess was", input    
    pass    
    f = simplegui.create_frame("Guess the number", 200, 200)  



f.add_input("Enter a guess", input_guess, 200)  


new_game()


