# Description
This app uses UDP communication to read gyro data from Parrot Minidrones (Rolling Spider or Mambo). The user can deploy a Simulink model on the hardware target. The app receives UDP packets from the Parrot Minidrone and plots gyro data in real time.

# How to use 
1.  Open Matlab and run "Parrot_minidrone_APP.mlapp"
2.  choose your hardware target from  "Select Target"
3.  Open the Simulink model from "Set Parameters & Build Model"
4.  Edit the model by pressing the "Edit model" button, the callback function configures the model to the hardware target chosen earlier in the "Select Target" pane and changes the transmitted variable from "ddz"(acceleration along z-axis) to "p" (angular rate ). the function change also the frequency of transmission from 1 Hz to 20 Hz.
5.  Build the model by pressing the "Build on Target" button, and wait until the Parrot Flight Control Interface is launched. Then press 'Start Button' from the same interface.
6.  Press the "Start Initialisation" button to initiate UDP transmission. You can choose the max execution time (by default the value is 30).
7.  Press the "Start" button to plot received data on the Axes. The user can press the " Stop" button to halt plotting data.
8.  The transmission is terminated if the max execution time is reached.   
9.  To restart a new transmission again, press the "Restart" button.
    
![Alt text](/tumbnail.JPG?raw=true "Title")
