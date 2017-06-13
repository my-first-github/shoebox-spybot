# shoebox-spybot
A RaspberryPi + Arduino based spybot

# Progress log
- **06/12/17**: 
  - Installed UBUNTU MATE + ROS on the Raspberry. 
  - Reinstalled UBUNTU GNOME 16.04 and ROS on the laptop. 
  - Configured VNC. 
  - Made this repository. 
  - Created base workspace. 
  - Created remote sourcing bash script (may need work as ROS_IP is being set blank). 
  - Tested remote sourcing bash script; works. 
  - Cloned and synced workspaces in both machines.   

- **06/13/17**
  - Created a simple teleop publisher to the *turtlesim_node*. Needs tuning to be used with the real robot.
  - Made a base level *action_input* wrapper to wrap around keyboard inputs.
  - Echoed commands from PC nodes to move the *turtlesim_node* running on the Raspberry Pi
  - As initially suspected, ROS_IP was being set blank, and this caused problems
  - Easily fixed, by replacing *wlan0* in the shellscript with *wlp2s0*
  - All of today's code resides in the *teleop_test* package

- **06/14/17**
  - Connected the camera to Raspberry Pi. Working on getting ffserver to work. Bad framerate. Trying to get 10 fps @ 320x240
  - Stumbled upon another interesting detail, UBUNTU MATE's spftware update utility is bugged
  - To update software on the Raspberry pi run *sudo apt update && sudo apt upgrade* and *sudo rpi-update*
  - Creating a shellscript for ffserver, so that the video feed can be accessed via browser from anywhere