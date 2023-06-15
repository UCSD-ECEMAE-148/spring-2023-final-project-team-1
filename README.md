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

- if time allows we also would like to add obstacle avoidance so that the car can make it home safely.

- I would be also nice to be able to detect is the program crashes or if a computer that is ssh’d into it loses connection 

## Video Demonstrations

### Controller Disconnect Detection 

[![IMAGE ALT TEXT](http://img.youtube.com/vi/uU5O4HXrWTc/0.jpg)](http://www.youtube.com/watch?v=uU5O4HXrWTc "Video Title")

### Full Demo

## What we have done

We modified the donkeycar drive script inside the path follow package manage.py. We added donkeycar parts for detecting controller disconnection. The way that we are detecting if the controller is disconnected is by using a threshold number. After a certain number of callbacks without controller inputs changing, it assumes that the controller is disconnected. We added a part to switch the pilot mode from user input to the path follow self driving pilot. Inside the this part we also added code to save the path from the starting (Home) position to the current position that it is at. It then inverts the path and loads the inverted path for the path follow pilot to use. We also attempted to add a part for the lidar. The lidar that we are using is not currently supported by donkeycar. We attempted to add a driver for the lidar we are using. We were able to recieve some data.

### What Worked

- We were able to detect controller disconnect. 

- We were also able to have the car return to the home postion.

### What didn't work as expected

- The lidar did not work as expected. We spent quite a few hours trying to make that work. Unfortunately, the lidar data was not clear enought for the car to make actionable decisions. Additonally, we noticed a large amount of delay in the data.

- The gps also in final testing stopped receiving data. Which was quite a set back. Unfortunately, we were unable to get a video of the car working before this happened.

### Possible Solutions

- One solution for the lidar would be to get the type of lidar that works better for donkeycar
- One solution for the gps would be to try a different gps

## If we had another week

If we had more time, we would like to have the car stop at once it has returned. More importantly, we would also very much like to get the lidar working and avoiding obstacles.





