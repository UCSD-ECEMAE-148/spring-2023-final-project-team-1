# Final Project
# ECE MAE 148 Spring 2023
![UCSD Logo](UCSDLogo.jpeg)
## Team 1 Members

Brandon Breeze - ECE
  
Liam Carmody - MAE
  
Dominic Orlando - ECE

## What we have promised

#### Must have

- Our idea is to have the robot car return to a pre-designated “Home Base” (GPS location) when it detects that is has disconnected from it’s controller. 

#### Nice to have

- Obstacle avoidance with the LD06 Lidar.

- Detection of program crash or ssh disconnection to then trigger the return home. 

## Video Demonstrations

### Controller Disconnect Detection 

[![IMAGE ALT TEXT](http://img.youtube.com/vi/uU5O4HXrWTc/0.jpg)](http://www.youtube.com/watch?v=uU5O4HXrWTc "Video Title")

### Full Demo
[![IMAGE ALT TEXT](http://img.youtube.com/vi/mMoTIyogB1E/0.jpg)](http://www.youtube.com/watch?v=mMoTIyogB1E "Video Title")

## Schematic


![Final project 148](https://github.com/UCSD-ECEMAE-148/spring-2023-final-project-team-1/assets/114778470/96904e35-b570-4fe2-b9a1-e34e59cb710e)


## What we have done

We modified the donkeycar drive script inside the path follow package manage.py. We added donkeycar parts for detecting controller disconnection. The way that we are detecting if the controller is disconnected is by using a threshold number. After a certain number of callbacks without controller inputs changing, it assumes that the controller is disconnected. We added a part to switch the pilot mode from user input to the path follow self driving pilot. Inside the this part we also added code to save the path from the starting (Home) position to the current position that it is at. It then inverts the path and loads the inverted path for the path follow pilot to use. We also added a part for the LD06 lidar since the LD06 lidar isn't supported by donkeycar. We also added a part that takes the lidar data as an input and adjusts the cross-track error accordingly.


### Parts added

- ControllerTest

- ChangeMode

- LD06Liar

- ObstacleDetector


### What Worked

- We were able to detect controller disconnect. 

- We were also able to have the car return to the home postion.

- When the ssh disconnects the script continues to run.

### What didn't work as expected

- While we were able to implement the LD06 lidar inside donkeycar, our current implementation is too delayed for a useful obstacle avoidance algoirhtm. Also it currently takes too long to run, hanging up the other parts of donkeycar. 

### Possible Solutions

- One solution would be to get an RPlidar or a similar lidar that is supported out of the box by Donkeycar

- There is potential to rewrite our part to get quicker measurements.
  
## If we had another week

If we had more time, we would like to have the car stop at once it has returned. More importantly, we would also very much like to get the lidar working and avoiding obstacles.

## Weekly Presentations
[Project Proposal](https://docs.google.com/presentation/d/1qEtfq2pOg_nVsMLH8ufqDtqr5y_wK0nWoPhvqwehMsQ/edit?usp=sharing)

[Weekly Update 1](https://docs.google.com/presentation/d/1sYh_EFIsonskD8AUsqKGqOPb3pKjL_P4ma7JfMe9Sg0/edit?usp=sharing)

[Final Presentation](https://www.beautiful.ai/player/-NY-q95_Cp7QaUgcc3yY)
