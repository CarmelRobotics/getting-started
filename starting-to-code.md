# Class Breakdown
This guide is going to assume that you were able to successfully installed FRC VS Code(a specific FRC coding framework program design 
for visual studios) and have a general understanding of java. If you don't have either of these things, it is going to be difficult for 
you to follow along. The reason why we don't explain any of these things here is because it would take a huge amount of time to explain 
these things and there are plenty of tutorials out there on java or setting of FRC VS Code already. Check of this doc that we made if 
you need additional help click [here](https://docs.google.com/document/d/1u8_LrAfO6XVPyn7fh2uA1ldmiwVRVrZO-xOsBdCmuu0/edit).

When you create a new java robot project(select command based as that's what we will be working in), the first thing that you will notice 
is that there are some classes automatically created for you and a huge list of directories and sub directories that are created for you.

The two main directories that you see right now are subsystems and commands. Outside those directories are RobotMap, Robot, OI, and main. 
We are going to go through each of these and explain how these work in the conception of a robot.


## Robot
This is the main class that we will be working in. All of the subsystems, commands, and OI created will be declared in this file. The 
most important things to look for in the robot class are '''robot init''' and '''robot periodic'''. The robot init method is called once 
when the robot is turned on and basically initializes all of the values that need to be initialized once. Things like oi.initalize go 
into this file. The robot periodic method is where most of the methods go that need to be called repeatedly in order to check some value
or do some function. Methods that constantly update the drivetrain according to the position of the joystick go into this method. 

## Subsystems
For those that don't know, a subsystem is classified as a smaller part of a working whole(the working whole being the robot and the 
smaller part being a specific part if the robot). A drive train is an example of a possible subsystem. So is an arm mechanism for 
picking up cube objects. The basic outline of a subsystem is simple, really. If you look in the example subsystem class, you will see a 
mostly empty class with a constructor. To create a subsystem, pretty much all you have to do is create local public variables before 
the constructor(these can be specific motors used in the subsystem or solenoids), construct them within the constructor, and create 
methods within the class that use those variables(such as a method to tell a victor speed controller to move a motor forward). Methods 
created in the subsystem class will be called in specific commands as desired.

## Commands
This is the folder where you will create your command classes. For those that don't know what a command is, a command is basically a way 
of organizing a series of methods that will be triggered at the press of a button(joystick button). If you click on the example command 
class, you will notice that there are pre-created methods for you there. The most important methods to notice are the Start command 
method and the End command method. The start command method will be activated when the joystick button is pressed and the end method 
will be called after the start method putting an end to whatever you want to do in the start method. It is important to notice that this
is regulated by the isFinished method which will call the end method if it returns true. Take some time to fully understand how these 
command methods work and interact with each other. It will save you a lot of frustration in the future. 

## OI
This stands for **O**bject **I**nterface. This is the class where you actually create the buttons that will call the commands that you 
looked at earlier. The key to this class is to keep yourself organized when it comes to creating the button objects, as they can get 
cluttered if you are not careful. It is also important to note that buttons cannot be created with the parameter value of 0. Button 
mapping always starts at 1 because joysticks don't have a button 0. Make sure to read the green readme text provided in the OI class 
before working with this class. It will give you useful tips for working with the class.

## RobotMap
This is the file where you will organize all of your variables via static reference. The variables declared in the robot map class are 
static in order for other classes to access them using the reference RobotMap.variableName. The variables used in RobotMap are usually 
final ints(PWM ports), joysticks, joystick buttons, numeric values for subsystems, and whatever else you may need to put in an 
accessible static class.

## Main
This is an interesting file that was added with the addition of FRC VS Code. You do not need to make any changes to this file but you 
have to make sure that the file is present otherwise the code won't compile.
