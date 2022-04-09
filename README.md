
# DFA MODULE

It is used to change or monitor the state of the state machine.


## Features

- Direct command send field
- State indicator field
- Custom Command button adding field
- Custom command button scroll field
- Quick State Changer Buttons


#### **Direct command send field:**
Lower input field, in which you can write a topic and directly send it to ```ADT/DFA/controllerFS/set``` by clicking on the **Send** button. After sending a command, 
the **Send** button will be disabled for a small amount of time while waiting for that command to be validated from the State Machine before sending a new one.

#### **State indicator image field:**

The responsive image field specifies the current 
state of the State Machine. The ***current state*** is colored in **green** and the rest is white.

#### **Custom command button adding field:**

###### *The upper input field:*


Specifies the
name of the custom button and the
one below that specifies the value 
of that button which is the string that will be sent to the right state machine topic (see this - link here - link to learn the topic ).  

Usage:

    1. Set the name of the button on the upper input field
    2. Set the value of the button on the lower input field or click on the ‘Copy’ button to set the value as the same as its name.
    3. Click on the ‘Add’ button to add this custom button to the Custom Command Button Scroll Area


#### **Custom command button scroll field:**

The buttons that are created in the custom command button add field are listed here. Click on any button to send its value to the right state machine topic. The field is also scrollable when needed.

After clicking on a custom button, the button will be colored in orange as the command is waiting for validation from the State Machine. And meanwhile, ALL the buttons in the field wil be disabled for that small amount of time.


#### **Quick State Changer Buttons:**
Those are the buttons under the state indicator image field.
 When clicked, they send the right command (‘start’,’stop’,’
 restart’ or ’reset’)  with respect to the current state and the
  value of the state button clicked. 

##### What is sends when clicked:


| Current State | Next State     | Command                       |
| :-------- | :------- | :-------- |
| `IDLE`      | `WORKING` | start|
| `IDLE`      | `WAITING` | ----|
| `WORKING`      | `WAITING` | stop|
| `WORKING`      | `IDLE` | reset|
| `WAITING`      | `WORKING` | restart|
| `WAITING`      | `IDLE` | reset|



