# Guide to getting started

## Setting up your environment

There are several things that you'll need to download in order to get started, this will explain how to download all of the programs that you may need.

### WPILIB Package

The most essential thing you'll need to get started is the WPILIB Package, found on [this page](https://github.com/wpilibsuite/allwpilib/releases) You’ll want to download the file from the assets called WPILIBInstaller_Window64 (it may have some numbers on the end to indicate the version).

Once it’s downloaded you’ll need to click on the file. It’ll open up in file explorer and you’ll see something similar to this.

![](https://github.com/CarmelRobotics/getting-started/blob/master/pics/wpilib_zip1.png)

Click on ```compressed folder tools > extract all > extract``` then once it is done copying the file, double click on the executable in the newly opened window and click run on the security warning. Then click current user.

You should see this. From here click on Select/Download VS Code and then Download. After VS Code has downloaded all you need to do is click on execute install and it will install the rest of the WPILIB elements.

![](https://github.com/CarmelRobotics/getting-started/blob/master/pics/wpi_installer.PNG)

### Git

Another program that is essential to our workflow is Git. The download can be found [here](https://git-scm.com/download/win). Once it’s downloaded just rapidly click through the setup until it gets to the install. The settings there only affect the command line git, which we do not use.

Another program that is essential to our workflow is Git. The download can be found [here](https://git-scm.com/download/win). Once it’s downloaded just rapidly click through the setup until it gets to the install. The settings there only affect the command line git, which we do not use.

## Cloning a Repository

### GitHub
If you would like to work on your robotics programming skills at home or want to code in the robotics team, then setting up a GitHub account is necessary. First you will need to go to github.com and sign up. From there all you will need to do is follow the site’s instructions for setting up an account. If you would like to become a member of the CarmelRobotics organization on GitHub, ask an owner of the organization in person or ask Clifford to invite you.

### Cloning, Pulling, Committing, and Pushing
Cloning and pulling are very similar and essentially save code from a GitHub repository onto your computer, specifically onto Visual Studio Code. The difference between cloning and pulling, however is that cloning is the first time a person would download the code onto their Visual Studio Code, while pulling is updating their version of the code to what is on GitHub's website. First copy the URL of the repository by opening the desired repository and clicking the clone or download repository and copying the URL. 

![](https://github.com/CarmelRobotics/getting-started/blob/master/pics/clone.PNG)

In order to pull, you will have to have Visual Studio Code opened and type Ctrl + Shift + P then type “Pull” and click on “Git: Pull”, then paste the URL and press enter.

Committing is essentially saving your code and preparing it for pushing which replaces the old code with your code on GitHub’s website. In order to commit, press Ctrl + Shift + P, then type “Commit”, click on “Git: Commit”, it will then require a message and explaining what you updated might be helpful, then press enter. Press Ctrl + Shift + P, then type “Push”, click the “Git: Push”.

## Ready
You are now ready to start coding. If you would like to learn Java go to [here](https://codecademy.com/learn/learn-java). Every year there is a new FRC API and getting the link to that will be necessary to know which methods you are able to call and use when coding.
